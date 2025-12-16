<script lang="ts">
	import { Button, TextArea, TextInput } from 'carbon-components-svelte';
	import { onMount } from 'svelte';
	import { image, title, subtitle } from '$lib/innerVariables';

	onMount(() => {
		$image =
			'https://contents.yrka.app/api/files/pbc_3945946014/440g761423pt82d/contact_us_person_eiurka2k1u.jpg';

		$title = 'Contact Us';

		$subtitle = 'YOUreka is more than a business!';
	});
</script>

<main>
	<section
		class="flex shadow-2xl w-fit mx-auto px-8 py-8 flex-col mt-12 items-center justify-center mb-12"
	>
		<div class="md:flex text-start justify-center md:gap-x-12 md:space-y-0 space-y-8 mt-12">
			<div class="flex gap-4 items-start">
				<div class="flex flex-col gap-4">
					<div class="flex items-center gap-4">
						<svg
							class="text-green-700 bg-white rounded-full p-1"
							xmlns="http://www.w3.org/2000/svg"
							width="35"
							height="35"
							viewBox="0 0 24 24"
							><path
								fill="currentColor"
								d="M19.95 21q-3.125 0-6.175-1.362t-5.55-3.863t-3.862-5.55T3 4.05q0-.45.3-.75t.75-.3H8.1q.35 0 .625.238t.325.562l.65 3.5q.05.4-.025.675T9.4 8.45L6.975 10.9q.5.925 1.187 1.787t1.513 1.663q.775.775 1.625 1.438T13.1 17l2.35-2.35q.225-.225.588-.337t.712-.063l3.45.7q.35.1.575.363T21 15.9v4.05q0 .45-.3.75t-.75.3"
							/></svg
						>
						<h4 class="font-semibold">Call us</h4>
					</div>
					<ul class="flex flex-col gap-2 text-gray-500">
						<li>+234-801-234-5678</li>
						<li>+234-802-345-6789</li>
					</ul>
				</div>
			</div>

			<div class="flex gap-4 items-start">
				<div class="flex flex-col gap-4">
					<div class="flex items-center gap-4">
						<svg
							class="text-green-700 bg-white rounded-full p-1"
							xmlns="http://www.w3.org/2000/svg"
							width="35"
							height="35"
							viewBox="0 0 24 24"
							><path
								fill="currentColor"
								d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2m0 4l-8 5l-8-5V6l8 5l8-5z"
							/></svg
						>
						<h4 class="font-semibold">Email us</h4>
					</div>
					<ul class="flex flex-col gap-2 text-gray-500">
						<li>contact@yrka.ng</li>
					</ul>
				</div>
			</div>

			<div class="flex gap-4 items-start">
				<div class="flex flex-col gap-4">
					<div class="flex items-center gap-4">
						<svg
							class="text-green-700 bg-white rounded-full p-1"
							xmlns="http://www.w3.org/2000/svg"
							width="35"
							height="35"
							viewBox="0 0 24 24"
							><path
								fill="currentColor"
								d="M12 11.5A2.5 2.5 0 0 1 9.5 9A2.5 2.5 0 0 1 12 6.5A2.5 2.5 0 0 1 14.5 9a2.5 2.5 0 0 1-2.5 2.5M12 2a7 7 0 0 0-7 7c0 5.25 7 13 7 13s7-7.75 7-13a7 7 0 0 0-7-7"
							/></svg
						>
						<h4 class="font-semibold">Visit us</h4>
					</div>
					<ul class="flex flex-col gap-2 text-gray-500">
						<li>University of Calabar</li>
						<li>PMB 1115, Calabar</li>
						<li>Cross River State, Nigeria</li>
					</ul>
				</div>
			</div>
		</div>

		<form action="" class="bg-white p-5 rounded-md mt-8 md:w-[700px]">
			<div class="md:grid md:grid-cols-2 gap-5">
				<TextInput size="sm" labelText="First & Last Name" placeholder="i.e. John Doe" />

				<TextInput size="sm" labelText="Email" placeholder="i.e. john@gmail.com" />

				<TextInput size="sm" labelText="Phone Number" placeholder="i.e. +1-234-567-8901" />

				<TextInput size="sm" labelText="Subject" placeholder="i.e. I need a help" />
			</div>

			<div class="mt-5">
				<TextArea labelText="Message" placeholder="Type your message" />
			</div>

			<div class="mt-5 text-start">
				<button type="submit" class="bg-green-600 p-3 px-8 text-white rounded-sm font-medium"
					>Send</button
				>
			</div>
		</form>
	</section>
</main>
