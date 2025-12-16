<script lang="ts">
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_3945946014/35779t189h2o9v7/problem_solution_fit_64922822_xxl_puzzle_piece_e1499237044963_230469358_2yzuut6fod.jpg';

		$title = 'Corporate Philosophy';

		$subtitle = 'YOUreka is more than a business!';
	});
</script>

<main>
	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">Vision</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<p class="text-lg md:text-xl">
				To be a global leader in leveraging technology for human development, advancing ideas into <br
				/> innovative solutions that serve humanity.
			</p>
		</div>
	</section>

	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">Mission</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<p class="text-lg md:text-xl">
				To create and implement frugal, innovative technology solutions that address the unique
				challenges <br /> of technology resource-limited settings, thereby fostering digital transformation
				across industries.
			</p>
		</div>
	</section>

	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">Goals</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<li>To lead the digital transformation in underserved regions.</li>
			<li>To create sustainable, scalable, and impactful technology solutions.</li>
			<li>
				To empower communities through accessible and innovative technological <br /> advancements.
			</li>
		</div>
	</section>

	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">Aims and Objectives</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<li>To develop and deploy cost-effective technology solutions.</li>
			<li>To promote digital inclusion and bridge the technology gap.</li>
			<li>To enhance the quality of life through technology-driven solutions.</li>
		</div>
	</section>

	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">Our Charter</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<p class="text-lg md:text-xl">
				YOUreka is dedicated to ethical practices, innovation, and inclusivity. We prioritise
				human-centric <br /> design and strive to ensure our solutions have a lasting, positive impact.
			</p>
		</div>
	</section>

	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">
			The <span class="text-green-500">YOU<span class="text-orange-500">re</span>ka</span> Way of Life
		</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<p class="text-lg md:text-xl">
				A commitment to continuous learning, innovation, and collaboration. We embrace challenges as <br
				/> opportunities to create solutions that transform (empower and prosper) humanity.
			</p>
		</div>
	</section>
</main>
