<script>
	import { site } from '$lib/site';
</script>

<header>
	<div class="inner">
		<div>
			<h1><a href="/"><img src="/logo.png" alt="logo"/></a></h1>
		</div>
		<div>
			<!-- svelte-ignore component-name-lowercase -->
			<nav>
				{#each site.nav as { label, href }}
					<a href="{href}">{label}</a>
				{/each}
			</nav>
		</div>
		<div>
			<a href="{`tel:${site.tel}`}" class="button">{site.tel}</a>
		</div>
	</div>
</header>

<style>
	header {
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 2em;
		box-shadow: 0 0.25em 1em -0.5em hsl(var(--clr-primary));
	}

	header > .inner {
		flex: 1;
		max-width: 1024px;
		display: flex;
		flex-flow: row wrap;
		justify-content: space-between;
		align-items: center;
		gap: 2rem;
		padding: 0 2rem;
	}

	h1 {
		text-transform: uppercase;
		font-size: 1.5em;
		margin: 0;
	}

	h1 > a {
		text-decoration: none;
	}

	h1 > a > img {
		width: 300px;
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

	@media (max-width: 500px) {
		header > .inner {
			justify-content: center;
			text-align: center;
		}
	}
</style>
