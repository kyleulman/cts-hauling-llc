<script>
	import { site } from '$lib/site';
	import { General } from '$lib/comps/general';

	const about = {
		heading: 'About',
		body: `<p>C&T's Hauling LLC is owned and operated by Cody Russ. While the business is focused around junk removal, our list of residential services is rapidly expanding.</p>`,
		cta: {
			action: 'https://calendly.com/ctshaulingllc',
			label: `Check out our new <wbr> pressure washing service!`
		},
		img: {
			src: '/truck-junk.jpg',
			alt: 'Truck junk',
			width: '1000',
			height: '750'
		}
	};
</script>

<svelte:head>
	<title>{about.heading} - {site.title}</title>
</svelte:head>

<General data={about} />
