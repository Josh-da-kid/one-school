<script lang="ts">
	import { page } from '$app/stores';
	import Dropdown from './Dropdown.svelte';

	let { mobileMenuOpen = $bindable(false), menuIcon = $bindable('fa-bars') } = $props();

	let companyMenuOpen = $state(false);
	let servicesMenuOpen = $state(false);

	// Get current path for active menu highlighting
	let currentPath = $derived($page.url.pathname);

	function toggleMenu() {
		mobileMenuOpen = !mobileMenuOpen;
		menuIcon = mobileMenuOpen ? 'fa-xmark' : 'fa-bars';
	}
</script>

<!-- {#if $page.url.pathname !== '/entity-type' && $page.url.pathname !== '/signup'} -->
<header class="w-full text-orange-500">
	<div class="flex flex-col max-w-7xl px-4 sm:px-6 py-5 md:py-8 mx-auto relative">
		<!-- Logo -->
		<a href="/" class="flex items-center gap-2 absolute left-4 sm:left-6 bottom-[-50px] z-30">
			<img
				src="/photo_2025-12-09_14-21-13.jpg"
				alt="youreka-logo"
				class="h-[100px] w-[100px] text-sky-400 rounded-b-full"
			/>
		</a>

		<!-- Desktop Nav -->
		<nav class="hidden justify-center mx-auto items-center space-x-8 font-semibold md:flex">
			<a
				href="/"
				class="hover:text-green-500 text-orange-500"
				class:border-b-2={currentPath === '/'}
				class:text-green-800={currentPath === '/'}
				class:opacity-80={currentPath === '/'}>Home</a
			>

			<Dropdown
				dropdownId="nav-2"
				selectedId="0"
				items={[
					{ id: '0', text: 'Our Company' }, // This will be unclickable
					{ id: '1', text: 'About Us', href: '/about' },
					{ id: '2', text: 'Institutional Framework', href: '/framework' },
					{ id: '3', text: 'Corporate Philosophy', href: '/philosophy' }
				]}
			/>

			<Dropdown
				dropdownId="nav-1"
				selectedId="0"
				items={[
					{ id: '0', text: 'Our Services' }, // This will be unclickable
					{ id: '1', text: 'AcademIQ', href: '/academiq' },
					{ id: '2', text: 'ClinIQ', href: '/cliniq' },
					{ id: '3', text: 'FUNDNet', href: '/fundnet' },
					{ id: '4', text: 'IDID', href: '/idid' },
					{ id: '5', text: 'LogistIQ', href: '/logistiq' },
					{ id: '6', text: 'Sydney Gateway', href: '/sydney-gateway' },
					{ id: '7', text: 'TriIQ', href: '/tri-iq' },
					{ id: '8', text: 'YOUlink', href: '/youlink' },
					{ id: '9', text: 'vMeetz MS', href: '/vmeetz-ms' }
				]}
			/>

			<a
				href="/contact"
				class="hover:text-green-500 text-orange-500"
				class:border-b-2={currentPath === '/contact'}
				class:text-green-800={currentPath === '/contact'}
				class:opacity-80={currentPath === '/contact'}>Contact Us</a
			>

			<a
				href="https://manage.yrka.ng/_/#/login"
				target="_blank"
				class="hover:text-green-500 text-orange-500"
				class:border-b-2={currentPath === '/manage'}
				class:text-green-800={currentPath === '/manage'}
				class:opacity-80={currentPath === '/manage'}>Manage Site</a
			>
		</nav>

		<!-- Mobile Menu Button -->
		<button
			id="menuToggle"
			class="text-2xl text-orange-500 focus:outline-none md:hidden self-end"
			on:click={toggleMenu}
		>
			<i class="fa-solid {menuIcon}"></i>
		</button>

		<!-- Mobile Menu -->
		<div
			id="mobileMenu"
			class="absolute top-16 left-0 w-full border-t border-gray-200 bg-white transition-all duration-300 md:hidden z-50"
			class:hidden={!mobileMenuOpen}
		>
			<div class="flex flex-col space-y-4 px-6 py-4 font-semibold">
				<a
					href="/"
					class="text-orange-500 hover:text-green-500"
					class:text-green-500={currentPath === '/'}
					class:font-bold={currentPath === '/'}>Home</a
				>
				<div class="flex flex-col">
					<button
						on:click={() => (companyMenuOpen = !companyMenuOpen)}
						class="flex justify-between items-center text-orange-500 font-semibold w-full"
					>
						<span>Our Company</span>
						<i class="fa-solid {companyMenuOpen ? 'fa-chevron-up' : 'fa-chevron-down'} text-sm"></i>
					</button>
					{#if companyMenuOpen}
						<div class="flex flex-col space-y-2 pl-4 pt-2">
							<a href="/about" class="hover:text-green-500 text-black">About Us</a>
							<a href="/framework" class="hover:text-green-500 text-black"
								>Institutional Framework</a
							>
							<a href="/philosophy" class="hover:text-green-500 text-black">Corporate Philosophy</a>
						</div>
					{/if}
				</div>

				<div class="flex flex-col">
					<button
						on:click={() => (servicesMenuOpen = !servicesMenuOpen)}
						class="flex justify-between items-center text-orange-500 font-semibold w-full"
					>
						<span>Our Services</span>
						<i class="fa-solid {servicesMenuOpen ? 'fa-chevron-up' : 'fa-chevron-down'} text-sm"
						></i>
					</button>
					{#if servicesMenuOpen}
						<div class="flex flex-col space-y-2 pl-4 pt-2">
							<a href="/academiq" class="hover:text-green-500 text-black">AcademIQ</a>
							<a href="/cliniq" class="hover:text-green-500 text-black">ClinIQ</a>
							<a href="/fundnet" class="hover:text-green-500 text-black">FUNDNet</a>
							<a href="/idid" class="hover:text-green-500 text-black">IDID</a>
							<a href="/logistiq" class="hover:text-green-500 text-black">LogistIQ</a>
							<a href="/sydney-gateway" class="hover:text-green-500 text-black">Sydney Gateway</a>
							<a href="/tri-iq" class="hover:text-green-500 text-black">TriIQ</a>
							<a href="/youlink" class="hover:text-green-500 text-black">YOUlink</a>
							<a href="/vmeetz-ms" class="hover:text-green-500 text-black">vMeetz MS</a>
						</div>
					{/if}
				</div>

				<a
					href="/contact"
					class="text-orange-500 hover:text-green-500"
					class:text-green-500={currentPath === '/contact'}
					class:font-bold={currentPath === '/contact'}>Contact Us</a
				>

				<a
					href="https://manage.yrka.ng/_/#/login"
					target="_blank"
					class="text-orange-500 hover:text-green-500"
					class:hover:text-green-500={currentPath !== '/manage'}
					class:text-green-500={currentPath === '/manage'}
					class:font-bold={currentPath === '/manage'}>Manage Site</a
				>
			</div>
		</div>
	</div>
</header>
<!-- {/if} -->
