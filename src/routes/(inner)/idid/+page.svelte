<script>
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/4j7e0ehkur169m0/biometrics_image_958301095_k6fm3ko8m1.jpg';

		$title = 'IDID';

		$subtitle = 'A YOUreka Service';
	});
</script>

<main>
	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-4xl md:text-5xl font-medium">the What?</h1>

		<div class="text-lg flex flex-col gap-8 py-5 px-4 md:text-2xl">
			<p>
				Intelligent Digital Identity (IDID) is an enterprise-grade, integrated digital identity
				solution for Identity and Access <br /> Management (IAM) and Identity Governance and Administration
				(IGA).
			</p>
		</div>
	</section>
</main>
