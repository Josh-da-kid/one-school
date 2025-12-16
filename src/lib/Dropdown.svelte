<script lang="ts">
	import { get } from 'svelte/store';
	import { page } from '$app/stores';

	export let items: { id: string; text: string; href?: string }[] = [];
	export let className: string = '';
	export let selectedId: string = '0';

	// Check if this dropdown is the one open
	import { openDropdown } from '$lib/dropdownstore';
	export let dropdownId: string;

	$: isOpen = $openDropdown === dropdownId;

	function toggle() {
		openDropdown.set(isOpen ? null : dropdownId);
	}

	function select(id: string) {
		selectedId = id;
		openDropdown.set(null); // close all
	}
</script>

<div class="relative">
	<!-- Trigger -->
	<button
		class="flex items-center justify-between rounded text-orange-500 px-3 py-2 font-bold {className}"
		on:click={toggle}
	>
		<span>{items[0].text}</span>
		<i class="fa-solid fa-chevron-down ml-2 text-sm"></i>
	</button>

	<!-- Dropdown menu -->
	{#if isOpen}
		<div class="animate-fadeIn absolute left-0 z-50 mt-2 w-[180px] border bg-white shadow-lg">
			{#each items.slice(1) as item (item.id)}
				{#if item.href}
					<a
						href={item.href}
						class="dropdown-item block cursor-pointer py-1 hover:bg-gray-100"
						class:bg-gray-200={$page.url.pathname === item.href}
						on:click={() => select(item.id)}
					>
						<div class="ml-3 p-2 px-3 text-black">
							{item.text}
						</div>
					</a>
				{:else}
					<div
						class="dropdown-item py-1"
						class:cursor-pointer={item.id !== '0'}
						class:hover:bg-gray-100={item.id !== '0'}
						on:click={() => item.id !== '0' && select(item.id)}
					>
						<div class="ml-3 p-2 px-3 font-semibold">{item.text}</div>
					</div>
				{/if}
			{/each}
		</div>
	{/if}
</div>

<style>
	@keyframes fadeIn {
		from {
			opacity: 0;
			transform: translateY(-4px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}
	.animate-fadeIn {
		animation: fadeIn 0.15s ease-out;
	}

	.dropdown-item {
		border-bottom: 1px solid #3e424d; /* Corresponds to Tailwind's gray-200 */
	}

	/* Remove bottom border from the last item */
	.last-item {
		border-bottom: none;
	}
</style>
