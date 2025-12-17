<script lang="ts">
	import { onMount } from 'svelte';
	import { page } from '$app/stores';
	import '../app.css';
	import 'carbon-components-svelte/css/all.css';
	import NavBar from '$lib/NavBar.svelte';
	import Footer from '$lib/Footer.svelte';

	let { children } = $props();

	// Mobile menu state
	let mobileMenuOpen = $state(false);
	let menuIcon = $state('fa-bars');
	let backToTopVisible = $state(false);

	// Mobile menu toggle
	function toggleMenu() {
		mobileMenuOpen = !mobileMenuOpen;
		menuIcon = mobileMenuOpen ? 'fa-xmark' : 'fa-bars';
	}

	// Back to top button visibility
	function handleScroll() {
		backToTopVisible = window.scrollY > 200;
	}

	function scrollToTop() {
		window.scrollTo({ top: 0, behavior: 'smooth' });
	}

	// Get current path for active menu highlighting
	let currentPath = $derived($page.url.pathname);

	onMount(() => {
		// Load external scripts
		const loadAOS = () => {
			const aosScript = document.createElement('script');
			aosScript.src = 'https://unpkg.com/aos@2.3.1/dist/aos.js';
			const initAOS = () => {
				if ((window as any).AOS) {
					(window as any).AOS.init({ once: true, duration: 800 });
				}
			};
			aosScript.onload = initAOS;
			document.head.appendChild(aosScript);
		};

		// Load AOS after a short delay
		setTimeout(loadAOS, 100);

		// Add scroll listener
		window.addEventListener('scroll', handleScroll);

		// Hide preloader
		setTimeout(() => {
			document.body.classList.add('loaded');
		}, 4000);

		return () => {
			window.removeEventListener('scroll', handleScroll);
		};
	});
</script>

<svelte:head>
	<link
		rel="icon"
		href="https://oneschool.yrka.app/images/photo_2025-10-26_16-16-28-removebg-preview.png"
	/>
	<meta charset="utf-8" />
	<title>YOUreka | IDea, Innovation, Industry</title>
	<meta name="viewport" content="width=device-width, initial-scale=1" />
	<meta name="theme-color" content="#0b63d8" />

	<!-- AOS CSS -->
	<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet" />

	<!-- Font Awesome -->
	<link
		rel="stylesheet"
		href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
	/>

	<!-- Iconify -->
	<script src="https://code.iconify.design/iconify-icon/2.1.0/iconify-icon.min.js"></script>
</svelte:head>

<main class="flex min-h-screen flex-col overflow-x-hidden">
	<!-- NAV -->
	<NavBar bind:mobileMenuOpen bind:menuIcon />

	{@render children()}

	<!-- FOOTER -->
	<Footer />
</main>
