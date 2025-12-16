<script>
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/enr92n25x329wd1/logistiqx_7ee3d4myhw.jpeg';

		$title = 'LogistIQ';

		$subtitle = 'A YOUreka Service';
	});
</script>

<main>
	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12 px-4">
		<h1 class="text-4xl md:text-5xl font-medium">the What?</h1>

		<div class="text-lg flex flex-col gap-8 py-5 md:text-2xl">
			<p>
				LogistIQ is a cutting-edge solution that is designed to revolutionize logistics. Our
				platform <br /> integrates advanced analytics, real-time tracking, and automated processes
				to streamline <br /> operations, reduce costs, and enhance overall efficiency. By leveraging
				LogistIQ, businesses can <br /> transform their traditional logistics frameworks into
				dynamic, data-driven ecosystems, ensuring <br /> seamless coordination and optimized performance
				across the entire supply chain.
			</p>
		</div>
	</section>
</main>
