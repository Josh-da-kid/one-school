<script lang="ts">
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_3945946014/b8xo1il61w643s9/idea_innovation_industry_b4vtim852m.jpg';

		$title = 'About YOUreka';

		$subtitle = 'YOUreka is more than a business!';
	});
</script>

<main>
	<section class="max-w-7xl items-center mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-center mx-auto text-4xl md:text-5xl font-medium">
			We are here to connect and empower the <br /> YOUreka community.
		</h1>

		<div class="text-lg flex flex-col gap-2 px-4">
			<p class="text-lg md:text-xl">
				YOUreka is a “Technology for Human Development (TechHD)” proposition.
			</p>

			<p class="text-lg md:text-xl">
				Yes, it is much more than just a business, company or organisation; it is a philosophy, a
				movement, and a way of life.
			</p>

			<p class="text-lg md:text-xl">
				In YOUreka we are passionately invested in leveraging new-age, cutting-edge technology to
				spearhead digital transformation, particularly in technology resource-constrained areas.
			</p>

			<p class="text-lg md:text-xl">
				Our brand identity is encapsulated in our motto: “IDea, Innovation, Industry” – which is a
				pledged commitment to advance “IDea to innovation and industry.”
			</p>

			<p class="text-lg md:text-xl">
				When we say YOUreka, it simply means, “We found it! . . . for YOU!!” “We’ll find it for
				YOU.” It reiterates commitment to stay restless and relentless in “innovating for humanity.”
			</p>
		</div>
	</section>
</main>
