<script>
	export let data;
</script>

<section>
	<article>
		<h2>{data.heading}</h2>
		<div>
			{@html data.body}
		</div>
		<a href={data.cta.action} class="button">{@html data.cta.label}</a>
	</article>
	<figure>
		<img
			src={data.img.src}
			alt={data.img.alt}
			width={data.img.width}
			height={data.img.height}
		/>
	</figure>
</section>

<style>
	section {
		display: flex;
		flex-flow: row wrap;
		justify-content: center;
		align-items: center;
		padding: 2rem;
		gap: 2rem;
	}

	h2 {
		font-size: 4rem;
	}

	article {
		max-width: 500px;
	}

	figure {
		flex: 1;
		margin: 0;
		max-width: 768px;
		min-width: 150px;
		height: auto;
	}

	img {
		width: auto;
		height: auto;
		filter: drop-shadow(0.33em 0.33em 0.25em hsl(var(--clr-primary)));
		border-radius: 50%;
	}
</style>
