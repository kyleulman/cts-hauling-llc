<script>
	import { site } from '$lib/site';
	import { General } from '$lib/comps/general';

	const services = {
		heading: 'Services',
		body: `<ul><li>Home Clean-Outs</li><li>Large Item Removal</li><li>Pressure Washing</li></ul><p>Our list is growing all the time!</p>`,
		cta: {
			action: 'https://calendly.com/ctshaulingllc',
			label: 'Ask about our residential services!'
		},
		img: {
			src: '/siding.jpg',
			alt: 'Siding',
			width: '1000',
			height: '750'
		}
	};
</script>

<svelte:head>
	<title>{services.heading} - {site.title}</title>
</svelte:head>

<General data={services} />
