<script>
	export let image;
	export let title;
	export let subtitle;
	export let height = '400px';
</script>

<section
	class="w-screen py-12 text-center items-center transition-all duration-500 md:flex relative"
	style:height
>
	<div class="absolute inset-0">
		<img src={$image} alt="" class="w-full h-full object-cover" />
		<div class="absolute inset-0 bg-gradient-to-r from-black/100 to-black/10"></div>
	</div>
	<div class="relative mx-auto mt-16 sm:mt-0 flex w-full max-w-7xl flex-col gap-4 p-4 px-8">
		<h4 class="text-white text-start text-xl md:text-2xl">
			{$subtitle}
		</h4>
		<h1 class="text-4xl font-bold text-white text-start md:text-7xl">
			{@html $title}
		</h1>
	</div>
</section>
