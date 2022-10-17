<script>
	import { site } from '$lib/site';

	import '$lib/css/_.css';
	import '$lib/css/app.css';

	import { Header } from '$lib/comps/header';
	import { Footer } from '$lib/comps/footer';
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap"
		rel="stylesheet"
	/>
	<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet" />
	<title>{site.title}</title>
	<meta name="description" content={site.description} />
	<meta property="og:image" content="/logo.jpg" />
</svelte:head>

<Header />
<main>
	<slot />
</main>
<Footer />
