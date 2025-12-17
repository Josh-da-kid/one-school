<script lang="ts">
	import Hero from '$lib/Hero.svelte';
	import { image, title, subtitle } from '$lib/innerVariables';
</script>

<svelte:head>
	<title>{$title ? `${$title} -` : ''}YOUreka | a TechHD</title>
</svelte:head>

<!-- Page banner, title, description -->

<Hero {image} {title} {subtitle} />

<slot />
