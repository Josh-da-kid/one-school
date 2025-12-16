<script lang="ts">
	import Hero from '$lib/Hero.svelte';
	import { image, title, subtitle } from '$lib/innerVariables';
</script>

<!-- Page banner, title, description -->

<Hero {image} {title} {subtitle} />

<slot />
