<script>
	import { site } from '$lib/site';

	const year = new Date().getFullYear();

	const footer = {
		copy: `&copy; ${year} ${site.title}`,
		socials: [
			{
				action: `https://instagram.com/ctshaulingllc`,
				src: `/instagram.svg`,
				alt: "C&T's Hauling LLC Instagram page",
				width: 48,
				height: 48,
			},
			{
				action: `https://facebook.com/ctshaulingllc`,
				src: `/facebook.svg`,
				alt: "C&T's Hauling LLC Facebook page",
				width: 48,
				height: 48,
			},
		],
	};
</script>

<section class="info">
	<article>
		<h2>{site.hours.heading}</h2>
		<div>{@html site.hours.body}</div>
	</article>
	<article>
		<h2>{site.location.heading}</h2>
		<div>{@html site.location.body}</div>
	</article>
</section>

<footer>
	<div>
		<p>
			<b class="title">{site.title}</b>
			<br />
			<small>{@html footer.copy}</small>
		</p>
	</div>

	<!-- svelte-ignore component-name-lowercase -->
	<nav>
		{#each site.nav as { label, href }}
			<a href="{href}">{label}</a>
		{/each}
	</nav>

	<div>
		<a href="https://calendly.com/ctshaulingllc">Make an Appointment Today</a>
	</div>
	<div class="socials">
		{#each footer.socials as social}
			<a href="{social.action}">
				<img src="{social.src}" alt="{social.alt}" width="{social.width}" height="{social.height}/Z" />
			</a>
		{/each}
	</div>
	<!-- prettier-ignore  -->
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
		<path 
			fill="hsl(var(--clr-secondary))" 
			fill-opacity="0.5" 
			d="M0,96L48,106.7C96,117,192,139,288,128C384,117,480,75,576,53.3C672,32,768,32,864,48C960,64,1056,96,1152,106.7C1248,117,1344,107,1392,101.3L1440,96L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
		</path>
	</svg>
</footer>

<style>
	.info {
		position: relative;
		display: flex;
		flex-flow: row wrap;
		justify-content: space-evenly;
		align-items: center;
		gap: 2rem;
		padding: 2rem;
		text-align: center;
	}

	.info > article {
		max-width: 400px;
		background: hsl(var(--clr-background));
		padding: 2rem;
		box-shadow: 0 0 1em hsl(var(--clr-primary));
		border-radius: 1em;
	}

	footer {
		position: relative;
		display: flex;
		flex-flow: row wrap;
		align-items: center;
		gap: 2rem;
		justify-content: space-between;
		padding: 2rem;
	}

	footer svg {
		position: absolute;
		left: 0;
		bottom: 0;
		z-index: -1;
	}

	nav {
		display: flex;
		gap: 1em;
	}

	nav > a {
		text-decoration: none;
		font-weight: 600;
		overflow-wrap: none;
	}

	.title {
		text-transform: uppercase;
	}

	.socials {
		display: flex;
		align-items: center;
		gap: 0.5em;
	}
</style>
