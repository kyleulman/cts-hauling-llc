<script>
	import { site } from '$lib/site';

	const home = {
		hook: `We love to haul your junk.`,
		value_prop: `Junk removal and residential services for Wilmington and the lower Cape Fear region.`,
		cta: {
			label: `Get a <em>FREE</em> estimate`,
			action: `https://calendly.com/ctshaulingllc`
		},
		featured_image: {
			src: `/truck-trailer-cutout.png`,
			alt: 'Truck trailer cutout'
		},
		featured_review: {
			body: `Super professional, punctual, and affordable! Hands down would recommend to anyone needs haul-away services and will definitely be using them again in the future!`,
			credit: `— Kaitlin on <a href="https://www.facebook.com/ctshaulingllc" target="_blank">Facebook</a>`
		},
		featured_services: {
			body: `We offer home clean-outs and large item removal. Our list of residential services is growing all the time. Check out our new pressure washing service!`,
			cta: {
				label: `See our full list of services`,
				action: `/services`
			},
			img: {
				src: `/truck-kids.jpg`,
				alt: `Truck kids`
			}
		}
	};
</script>

<svelte:head>
	<title>{home.hook} - {site.title}</title>
</svelte:head>

<section class="hero">
	<div class="inner">
		<article>
			<h2>
				<q>
					{home.hook}
				</q>
			</h2>
		</article>
		<article>
			<p>{home.value_prop}</p>
			<a href={home.cta.action} class="button">{@html home.cta.label}</a>
		</article>
	</div>
</section>
<section class="featured-image">
	<figure>
		<img src={home.featured_image.src} alt={home.featured_image.alt} />
	</figure>
</section>
<section class="featured-review">
	<span class="big-quote">&ldquo;</span>
	<article>
		<p>
			{home.featured_review.body}
		</p>
		<p>
			{@html home.featured_review.credit}
		</p>
	</article>
	<span class="big-quote">&rdquo;</span>
	<!-- prettier-ignore  -->
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" class="svg-top">
		<path 
			fill="hsl(var(--clr-secondary))" 
			fill-opacity="0.5" 
			d="M0,32L48,37.3C96,43,192,53,288,96C384,139,480,213,576,218.7C672,224,768,160,864,160C960,160,1056,224,1152,218.7C1248,213,1344,139,1392,101.3L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
		</path>
	</svg>
	<!-- prettier-ignore  -->
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" class="svg-bottom">
		<path 
			fill="hsl(var(--clr-secondary))" 
			fill-opacity="0.5" 
			d="M0,64L48,64C96,64,192,64,288,90.7C384,117,480,171,576,160C672,149,768,75,864,58.7C960,43,1056,85,1152,106.7C1248,128,1344,128,1392,128L1440,128L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z">
		</path>
	</svg>
</section>
<section class="services">
	<div class="inner">
		<figure>
			<img src={home.featured_services.img.src} alt={home.featured_services.img.alt} />
		</figure>
		<article>
			<p>{home.featured_services.body}</p>
			<a href={home.featured_services.cta.action} class="button"
				>{home.featured_services.cta.label}<span class="material-icons">east</span></a
			>
		</article>
	</div>
</section>

<style>
	.hero {
		display: flex;
		justify-content: center;
		align-items: center;
		margin: 2rem 0;
		padding: 0 2rem;
	}

	.hero > .inner {
		max-width: 1024px;
		display: flex;
		flex-flow: row wrap;
		align-items: center;
		justify-content: center;
	}

	.hero > .inner > article:last-child {
		display: flex;
		flex-flow: row wrap;
		justify-content: center;
		align-items: center;
		gap: 2em;
	}

	.featured-image {
		margin: 2rem 0;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.featured-image img {
		filter: drop-shadow(0.33em 0.33em 0.25em hsl(var(--clr-primary)));
	}

	.featured-review {
		padding: 0 2rem;
		margin: 2rem 0;

		position: relative;
		display: flex;

		justify-content: center;
		align-items: center;

		background: hsl(var(--clr-secondary) / 0.5);
	}

	.featured-review svg.svg-top {
		position: absolute;
		left: 0;
		right: 0;
		bottom: 100%;
		z-index: -1;
	}
	.featured-review svg.svg-bottom {
		position: absolute;
		left: 0;
		right: 0;
		top: 100%;
		z-index: -1;
	}

	.featured-review > article {
		padding: 2rem;
	}

	.featured-review p {
		font-size: 1.5rem;
		font-style: italic;
		line-height: 1.33;
	}

	.featured-review .big-quote:first-of-type {
		align-self: flex-start;
	}
	.featured-review .big-quote:last-of-type {
		align-self: flex-end;
	}

	.services {
		margin: 2rem 0;
		padding: 0 2rem;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.services > .inner {
		display: flex;
		flex-flow: row wrap;
		justify-content: center;
		align-items: center;
		gap: 2rem;
	}

	.services figure {
		margin: 0;
	}

	.services img {
		border-radius: 50%;
		box-shadow: 0.33em 0.33em 1em hsl(var(--clr-primary));
	}

	.services > .inner > article {
		display: flex;
		flex-flow: column;
		align-items: flex-start;
	}

	.services .button {
		display: flex;
		flex-flow: row nowrap;
		justify-content: flex-start;
		align-items: center;
		gap: 0.5em;
	}

	h2 {
		font-size: 4rem;
		min-width: 440px;
		text-align: center;
	}

	p {
		max-width: 500px;
		font-weight: 600;
	}

	.big-quote {
		font-size: 5rem;
	}

	@media (max-width: 500px) {
		h2 {
			min-width: 100%;
			text-align: center;
			font-size: 3rem;
		}

		.hero > .inner > article:last-child {
			justify-content: center;
			text-align: center;
		}

		.featured-review {
			padding: 1rem;
		}

		.featured-review article {
			padding: 1rem;
		}

		.services > .inner > article {
			display: flex;
			justify-content: center;
			align-items: center;
			text-align: center;
		}
	}
</style>
