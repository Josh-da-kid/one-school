<script>
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/3237h5715151i62/k_26_n_19121_lyj0421_5_funding_1_mj979lz9xm.jpg';

		$title = 'FUNDNet';

		$subtitle = 'A YOUreka Service';
	});
</script>

<main>
	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-4xl md:text-5xl font-medium">the What?</h1>

		<div class="text-lg flex flex-col gap-8 py-5 px-4 md:text-2xl">
			<p>
				FUNDNet is a cutting-edge platform that leverages advanced digital identity verification and
				secure <br /> governance protocols to ensure transparent and reliable crowdfunding experiences.
			</p>
		</div>
	</section>

	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12 px-4">
		<h1 class="text-4xl md:text-5xl font-medium">the Why?</h1>

		<div class="text-lg flex flex-col gap-8 py-5 px-4 md:text-2xl">
			<p>
				FundNet is a game-changer! It's a major step forward in how we fund projects together. It
				lets <br /> people like you invest in new ideas, helping to spark innovation, create jobs,
				and build a strong <br /> economy for everyone.
			</p>

			<p>
				FundNet is a game changer! It's a novel innovation in the crowdsourced-funding space. With <br
				/> FundNet . . .
			</p>
		</div>
	</section>
</main>
