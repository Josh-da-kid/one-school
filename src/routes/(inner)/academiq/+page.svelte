<script lang="ts">
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/u52p8f66elvo107/academiq_1bzbzyw0cs.jpeg';

		$title = 'AcademIQ';

		$subtitle = 'YOUreka is more than a business!';
	});
</script>

<main>
	<section class="max-w-7xl px-4 mx-auto flex flex-col gap-5 py-12">
		<h1 class="text-4xl md:text-5xl font-medium px-3">What's AcademIQ About</h1>

		<div class="text-lg flex flex-col gap-8 py-5 px-4 md:text-2xl">
			<p>
				AcademIQ is a cutting-edge digital solution transforming education from early learning to
				advanced <br /> research. It provides personalized learning paths, real-time feedback, and
				collaborative tools, <br /> fostering a dynamic and engaging educational experience for students
				and educators alike.
			</p>

			<p>
				AcademIQ is a state-of-the-art educational platform that revolutionizes learning for all
				ages. <br /> Offering customized curricula, immediate evaluations, and teamwork tools, it
				cultivates an active, <br /> stimulating learning atmosphere for both students and teachers.
				With AcademIQ, education knows <br /> no limits, enabling students to realize their full potential
				in a constantly changing world.
			</p>

			<p>
				A digital education transformation solution revolutionising education service delivery from
				itinerant <br /> to tertiary education systems, both formal and non-formal.
			</p>
		</div>
	</section>
</main>
