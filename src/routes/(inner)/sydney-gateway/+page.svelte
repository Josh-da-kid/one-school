<script>
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_863811952/ssc8n93838xzv4j/th_1002509382_dh0aafax2s.jpg';

		$title = 'Sydney Gateway';

		$subtitle = 'A YOUreka Service';
	});
</script>

<main>
	<section class="max-w-7xl mx-auto flex flex-col gap-5 py-12 px-4">
		<h1 class="text-4xl md:text-5xl font-medium">the What?</h1>

		<div class="text-lg flex flex-col gap-8 py-5 md:text-2xl">
			<p>
				SMS to Web technology seamlessly bridges the gap between traditional text messaging and the <br
				/>
				vast capabilities of the internet. It enables users to send SMS messages that trigger web-based
				<br />
				actions, such as updating databases, initiating transactions, or accessing real-time information.
				<br />
				This technology finds applications in various sectors, including banking, healthcare, and logistics,
				<br />
				where instant communication and data integration are crucial. YOUreka's SMS to Web service
				<br />
				offers a reliable and secure platform for businesses to leverage the power of SMS messaging to
				<br /> enhance their web-based applications and services.
			</p>
		</div>
	</section>
</main>
