<script>
	import { onMount } from 'svelte';
	let currentSlide = $state(0);

	const slides = [
		{
			image:
				'https://contents.yrka.app/api/files/pbc_3025951362/537o6egccvmffo7/function_fame_un5cyoctbm.jpeg'
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_3025951362/lsti3dsg19qb211/brain_light_bulbs_ideas_new_ideas_with_innovative_technology_creativity_generative_ai_15083_1124_5ookvdtu7a.jpg'
		},
		{
			image: '/background-video.mp4'
		}
	];

	const missions = [
		{
			image:
				'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTGk_085m2oXbUbn1o5nxapxOby62vgt_Pl3g&s',
			title: 'Our Vision',
			description:
				'To be a global leader in leveraging technology for human development, advancing ideas into innovative solutions that serve humanity.'
		},
		{
			image:
				'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTDpJJEpnPtA30yoZOqluVJSxjmoc_Mvi6kze2BDccNu1P-1AOxwWCVWB3XfN59lk-1IlI&usqp=CAU',
			title: 'Our Mission',
			description:
				'To create and implement frugal, innovative technology solutions that address the unique challenges of technology resource-limited settings, thereby fostering digital transformation across industries.'
		},
		{
			image:
				'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQjgHc0N28NxMMC88CiLR-Z9FT7At2q8_t2nq4EF5PtjUPyYYjftzQoyHxmcS7REoEiFa0&usqp=CAU',
			title: 'Our Charter',
			description:
				'YOUreka is dedicated to ethical practices, innovation, and inclusivity. We prioritise human-centric design and strive to ensure our solutions have a lasting, postive impact.'
		},
		{
			image:
				'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR_GedkJkodBY4Idb-NfEtcw8KnkqvPQMY77AILWxRpTk19noHDL0hcBVE5qUH03G7-vNQ&usqp=CAU',
			title: 'The YOUreka Way of Life',
			description:
				'A commitment to continuous learning, innovation, and collboration. We embrace challenges as opportunities to create solutions that trasnform (empower and prosper) humanity.'
		}
	];

	const frameworks = [
		{
			image:
				'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTGk_085m2oXbUbn1o5nxapxOby62vgt_Pl3g&s',
			title: 'Our Staff',
			description:
				' Simplify workflows, track professional development, and enhance student engagement. <br><br> Our team consists of passionate, innovative, and dedicated professionals who are committed to advancing our mission and vision.'
		},
		{
			image:
				'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTDpJJEpnPtA30yoZOqluVJSxjmoc_Mvi6kze2BDccNu1P-1AOxwWCVWB3XfN59lk-1IlI&usqp=CAU',
			title: 'Our Curriculum',
			description:
				'Integrate real-world applications, foster critical thinking, and encourage creativity in learning. <br><br> Our curriculum is designed with a focus on experiential learning, ensuring that students can connect theory with practice.'
		},
		{
			image:
				'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQjgHc0N28NxMMC88CiLR-Z9FT7At2q8_t2nq4EF5PtjUPyYYjftzQoyHxmcS7REoEiFa0&usqp=CAU',
			title: 'Administration',
			description:
				'Our administrative structure is designed to support agility and responsiveness, ensuring efficient implementation of our projects. <br><br> Our facilities are equipped with modern technology and designed to support various learning styles, enhancing the overall educational experience.'
		},
		{
			image:
				'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR_GedkJkodBY4Idb-NfEtcw8KnkqvPQMY77AILWxRpTk19noHDL0hcBVE5qUH03G7-vNQ&usqp=CAU',
			title: 'Governance',
			description:
				'Our governance framework includes a board of directors and executive management team that provides strategic direction and oversight. <br><br> Our facilities are equipped with modern technology and designed to support various learning styles, enhancing the overall educational experience.'
		}
	];

	const solutions = [
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/u52p8f66elvo107/academiq_1bzbzyw0cs.jpeg',
			title: 'AcademIQ',
			description:
				'A digital education transformation solution revolutionising education service delivery from itinerant to tertiary education systems, both formal and non-formal.'
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/152a0fhc2ylifh4/cliniq_2sw59gnmgq.jpeg',
			title: 'ClinIQ',
			description:
				'ClinIQx is an enterprise Software-as-a-Service solution for healthcare services delivery, administration, and governance. It stands out as patient-centred electronic health information and records management. '
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/3237h5715151i62/k_26_n_19121_lyj0421_5_funding_1_mj979lz9xm.jpg',
			title: 'FUNDNet',
			description:
				"An innovative crowdfunding platform powered by intelligent digital identity and assured governance. <br> FundNet is a game changer! It's a novel innovation in the crowdsourced-funding space. With FundNet . . ."
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/4j7e0ehkur169m0/biometrics_image_958301095_k6fm3ko8m1.jpg',
			title: 'IDID',
			description:
				'Intelligent Digital Identity (IDID) is an enterprise-grade, integrated digital identity solution for Identity and Access Management (IAM) and Identity Governance and Administration (IGA). '
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/enr92n25x329wd1/logistiqx_7ee3d4myhw.jpeg',
			title: 'LogistIQ',
			description:
				'A technology solution for logistics service system transformation.  <br> A technology solution for logistics service system transformation. '
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/ssc8n93838xzv4j/th_1002509382_dh0aafax2s.jpg',
			title: 'Sydney Gateway',
			description: 'SMS to web technology...'
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/44vb5mhz4m6afrw/triniqx_e167a6yn48.jpeg',
			title: 'TriIQ',
			description:
				'An intelligent, integrated transport manifest management, ride-hailing, and ride-sharing services solution.'
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/1i89mam82b36c31/youlink_as3xqy7kvb.jpeg',
			title: 'YOUlink',
			description:
				'A smart data communication service system for technology resource-limited settings, creating robust and reliable internet ecosystems.  '
		},
		{
			image:
				'https://contents.yrka.app/api/files/pbc_863811952/4f402211c10iqyq/vmeetz_t2e7lsfbln.jpeg',
			title: 'vMeetz MS',
			description:
				'vMeetz Media Service (MS) is an enterprise solution for managing physical and virtual meetings. It offers digital access management, digital security management, digital ticket sales, digital media services, and more.'
		}
	];

	onMount(() => {
		const interval = setInterval(() => {
			currentSlide = (currentSlide + 1) % slides.length;
		}, 5000);

		return () => clearInterval(interval);
	});

	// Helper to check if the current slide is a video
	let isVideo = $derived(slides[currentSlide]?.image.endsWith('.mp4'));
</script>

<main class="">
	<!-- hero section -->
	<section
		class="min-h-screen w-screen items-center bg-cover bg-center bg-no-repeat py-12 text-center transition-all duration-500 md:flex relative"
		style={!isVideo
			? `background-image: linear-gradient(to right, rgba(0, 0, 0, 1), rgba(0, 0, 0, 0.2)), url('${slides[currentSlide].image}');`
			: ''}
	>
		{#if isVideo}
			<video
				src={slides[currentSlide].image}
				autoplay
				loop
				muted
				playsinline
				class="absolute inset-0 w-full h-full object-cover z-0"
			></video>
			<div
				class="absolute inset-0 w-full h-full bg-gradient-to-r from-black/90 to-black/40 z-10"
			></div>
		{/if}
		<div class="relative mx-auto flex w-full max-w-7xl flex-col gap-12 p-4 px-8 z-20">
			<h4 class="text-white text-start text-xl md:text-2xl mt-6">
				YOUreka is more than a business!
			</h4>
			<h1 class="text-4xl font-bold text-white text-start md:text-7xl">
				We are <span class="curvy-underline">dedicated</span> to <br /> finding and creating <br />
				Innovative solutions <br /> For You
			</h1>

			<button
				class=" flex md:w-[300px] justify-center gap-3 bg-sky-400 p-4 text-center text-2xl md:text-3xl font-semibold text-white"
				>Join Us
			</button>

			<!-- slider button -->
			<div class="mt-4 flex justify-center items-center mx-auto">
				{#each slides as _, i}
					<button
						title="slide"
						class="mx-2 h-4 w-4 rounded-full {currentSlide === i ? 'bg-sky-500' : 'bg-gray-300'}"
						onclick={() => (currentSlide = i)}
					></button>
				{/each}
			</div>
		</div>
	</section>

	<section class="py-12 text-center flex flex-col gap-3 px-8 bg-sky-100/60">
		<h2 class="font-semibold text-3xl md:text-5xl">
			Our <span class="text-green-500">Cor<span class="text-orange-500"> por</span>ate</span> Philosophy
		</h2>
		<p class="text-lg">YOUreka represents a philosophy, a movement, and a way of life</p>

		<div class="grid md:grid-cols-2 lg:grid-cols-4 items-start mx-auto gap-4 max-w-7xl mt-8">
			{#each missions as i}
				<div class="flex flex-col gap-5 text-start shadow-2xl h-[500px]">
					<img src={i.image} alt={i.title} class="w-full object-cover h-48" />
					<div class="flex flex-col gap-4 px-4 md:px-8 py-4">
						<h4 class="text-start font-semibold text-3xl md:text-4xl">{i.title}</h4>
						<p class="text">{i.description}</p>
					</div>
				</div>
			{/each}
		</div>

		<button
			class="bg-green-500 w-fit text-white p-4 px-8 items-center text-center flex mx-auto mt-5 font-semibold text-lg mb-6"
			>Learn More</button
		>
	</section>

	<section class="py-12 flex flex-col gap-3 px-8 max-w-7xl mx-auto">
		<h2 class="font-semibold text-3xl md:text-5xl">
			<span class="text-green-500">YOU<span class="text-orange-500"> re</span>ka</span> Institutional
			Framework
		</h2>
		<!-- <p class="text-lg">YOUreka represents a philosophy, a movement, and a way of life</p> -->

		<div class="grid md:grid-cols-2 lg:grid-cols-2 items-start mx-auto gap-8 max-w-7xl mt-8">
			{#each frameworks as i}
				<div class="md:flex gap-3 text-start shadow-2xl lg:h-[320px]">
					<img src={i.image} alt={i.title} class="w-full md:w-[250px] h-full object-cover" />
					<div class="flex flex-col gap-4 px-4 md:px-8 py-4">
						<h4 class="text-start font-medium text-3xl md:text-4xl">{i.title}</h4>

						<p class="text">{@html i.description}</p>
					</div>
				</div>
			{/each}
		</div>

		<button
			class="bg-green-500 w-fit text-white p-4 px-8 items-center text-center flex mx-auto mt-5 font-semibold text-lg mb-6"
			>Learn More</button
		>
	</section>

	<section class="py-12 text-center flex flex-col gap-3 px-8 bg-sky-100/60">
		<h2 class="font-semibold text-3xl md:text-5xl text-green-500">Our Solutions</h2>
		<p class="text-lg">YOUreka represents a philosophy, a movement, and a way of life</p>

		<div class="grid md:grid-cols-2 lg:grid-cols-3 items-start mx-auto gap-8 max-w-7xl mt-8">
			{#each solutions as i}
				<div class="flex flex-col gap-5 text-start shadow-2xl h-[500px]">
					<img src={i.image} alt={i.title} class="w-full object-cover h-48" />
					<div class="flex flex-col gap-4 px-4 md:px-8 py-4">
						<h4 class="text-start font-semibold text-3xl md:text-4xl">{i.title}</h4>
						<p class="text">{@html i.description}</p>
					</div>
				</div>
			{/each}
		</div>
	</section>
</main>
