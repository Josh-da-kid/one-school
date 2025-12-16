<script>
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/4f402211c10iqyq/vmeetz_t2e7lsfbln.jpeg';

		$title = 'vMeetz MS';

		$subtitle = 'A YOUreka Service';
	});
</script>

<main>
	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12 px-4">
		<h1 class="text-4xl md:text-5xl font-medium">the What?</h1>

		<div class="text-lg flex flex-col gap-8 py-5 md:text-2xl">
			<p>
				vMeetz Media Service (MS) is an enterprise solution for managing physical and virtual
				meetings. It <br /> offers digital access management, digital security management, digital
				ticket sales, digital media <br /> services, and more.
			</p>
		</div>
	</section>
</main>
