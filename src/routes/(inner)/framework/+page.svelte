<script lang="ts">
	import { onMount } from 'svelte';

	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_3945946014/1y5p397m66l7p29/2008_new_challenges_for_corporate_governance_434atvj5sx.jpg';

		$title = 'Institutional Framework';

		$subtitle = 'YOUreka is more than a business!';
	});
</script>

<main>
	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">
			The <span class="text-green-500">YOU<span class="text-orange-500">re</span>ka</span> People
		</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<p class="text-lg md:text-xl">
				Our team consists of passionate, innovative, and dedicated professionals with diverse
				backgrounds <br /> and expertise, all committed to advancing our mission and vision through
				<br />
				collaborative efforts and continuous improvement.
			</p>
		</div>
	</section>

	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">Administration</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<p class="text-lg md:text-xl">
				Our administrative structure is designed to support agility and responsiveness, ensuring
				efficient <br /> implementation of our projects, and fostering a culture of innovation and
				collaboration across all <br /> departments.
			</p>
		</div>
	</section>

	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">Governance</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<p class="text-lg md:text-xl">
				Our governance framework is built upon a foundation of transparency and accountability,
				featuring a <br /> dedicated board of directors and an experienced executive management team
				that provides <br /> strategic direction, diligent oversight, and ensures alignment with our core
				values and objectives.
			</p>
		</div>
	</section>
</main>
