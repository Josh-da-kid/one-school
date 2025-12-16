<script>
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/1i89mam82b36c31/youlink_as3xqy7kvb.jpeg';

		$title = 'YOUlink';

		$subtitle = 'A YOUreka Service';
	});
</script>

<main>
	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12 px-4">
		<h1 class="text-4xl md:text-5xl font-medium">the What?</h1>

		<div class="text-lg flex flex-col gap-8 py-5 md:text-2xl">
			<p>
				YOUlink is a cutting-edge data communication service designed to thrive in environments with <br
				/>
				limited technological resources. Our system creates resilient and dependable internet ecosystems,
				<br />
				ensuring seamless connectivity and efficient data transfer even in challenging conditions. We
				<br />
				empower communities and organizations to overcome connectivity barriers and unlock the full
				<br /> potential of digital communication.
			</p>
		</div>
	</section>
</main>
