<script>
	import { site } from '$lib/site';
	import { General } from '$lib/comps/general';

	const contact = {
		heading: 'Contact',
		body: `<p>Call Cody at <a href="tel:9102644514">910-264-4514</a> or make an appointment online below to get a free estimate.</p>`,
		cta: {
			action: 'https://calendly.com/ctshaulingllc',
			label: `Get a <em>FREE</em> estimate`
		},
		img: {
			src: '/boxes.jpg',
			alt: 'Boxes',
			width: '1000',
			height: '750'
		}
	};
</script>

<svelte:head>
	<title>{contact.heading} - {site.title}</title>
</svelte:head>

<General data={contact} />
