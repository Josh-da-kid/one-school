<script lang="ts">
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/152a0fhc2ylifh4/cliniq_2sw59gnmgq.jpeg';

		$title = 'ClinIQ';

		$subtitle = 'YOUreka is more than a business!';
	});
</script>

<main>
	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12 px-4">
		<h1 class="text-4xl md:text-5xl font-medium px-3">What's ClinIQ About</h1>

		<div class="text-lg flex flex-col gap-8 py-5 px-4 md:text-2xl">
			<p>
				ClinIQx is an enterprise Software-as-a-Service solution for healthcare services delivery, <br
				/>
				administration, and governance. It stands out as patient-centred electronic health information
				and <br /> records management, enhancing care coordination even among organisations without
				EHR <br /> systems.
			</p>

			<p>
				ClinIQx represents a revolutionary Software-as-a-Service solution, expertly crafted to
				transform <br /> healthcare delivery, streamline administration, and enhance governance. Our
				innovative, patient-centric <br /> platform elevates electronic health information and
				revolutionizes records management, <br /> promoting seamless care coordination across a wide
				array of organizations, including those without <br /> established EHR systems. Step into
				the future of interconnected healthcare excellence with <br /> ClinIQx, where efficiency meets
				unparalleled patient care.
			</p>
		</div>
	</section>
</main>
