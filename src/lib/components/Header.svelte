<script lang="ts">
	import { onMount } from 'svelte';

	let isScrolled = $state(false);

	onMount(() => {
		const handleScroll = () => {
			isScrolled = window.scrollY > 50;
		};

		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});
</script>

<header 
	class="fixed top-0 left-0 w-full z-50 transition-all duration-300 py-6 px-8 flex items-center justify-between {isScrolled ? 'bg-black/90 backdrop-blur-md text-white shadow-sm py-4' : 'bg-transparent text-white'}"
>
	<div class="flex items-center gap-12">
		<a href="/" class="text-3xl md:text-4xl font-serif tracking-wide text-white hover:opacity-90 transition-opacity">
			DiligenceSquared
		</a>
		
		<nav class="hidden lg:flex items-center gap-8 text-sm font-medium text-gray-200">
			<div class="group relative cursor-pointer flex items-center gap-1 hover:text-white transition-colors">
				Platform
				<svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:rotate-180"><path d="m6 9 6 6 6-6"/></svg>
			</div>
			<div class="group relative cursor-pointer flex items-center gap-1 hover:text-white transition-colors">
				Solutions
				<svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:rotate-180"><path d="m6 9 6 6 6-6"/></svg>
			</div>
			<a href="#" class="hover:text-white transition-colors">Customers</a>
			<a href="#" class="hover:text-white transition-colors">Security</a>
			<div class="group relative cursor-pointer flex items-center gap-1 hover:text-white transition-colors">
				Resources
				<svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:rotate-180"><path d="m6 9 6 6 6-6"/></svg>
			</div>
			<div class="group relative cursor-pointer flex items-center gap-1 hover:text-white transition-colors">
				About
				<svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:rotate-180"><path d="m6 9 6 6 6-6"/></svg>
			</div>
		</nav>
	</div>

	<div class="flex items-center gap-6">
		<a href="#" class="text-sm font-medium hover:text-gray-300 transition-colors">Login</a>
	</div>
</header>
