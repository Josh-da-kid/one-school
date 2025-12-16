<script>
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/44vb5mhz4m6afrw/triniqx_e167a6yn48.jpeg';

		$title = 'TrilIQ';

		$subtitle = 'A YOUreka Service';
	});
</script>

<main>
	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12 px-4">
		<h1 class="text-4xl md:text-5xl font-medium">the What?</h1>

		<div class="text-lg flex flex-col gap-8 py-5 md:text-2xl">
			<p>
				TriIQ offers an all-in-one solution for managing transport manifests, ride-hailing, and
				ride-sharing <br /> services. Our intelligent platform integrates seamlessly with existing
				systems, optimizing routes, <br /> reducing costs, and enhancing the overall transportation
				experience for both providers and users. <br /> With TriIQ, you can streamline operations, improve
				efficiency, and deliver superior service.
			</p>
		</div>
	</section>
</main>
