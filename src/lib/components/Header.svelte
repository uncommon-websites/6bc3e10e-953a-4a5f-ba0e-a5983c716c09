<script>
	import { onMount } from 'svelte';

	let isScrolled = false;

	onMount(() => {
		const handleScroll = () => {
			isScrolled = window.scrollY > 50;
		};

		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});
</script>

<header 
	class="fixed top-0 left-0 w-full z-50 transition-all duration-300 py-6 px-8 flex items-center justify-between {isScrolled ? 'bg-white text-black shadow-sm py-4' : 'bg-transparent text-white'}"
>
	<div class="flex items-center gap-12">
		<a href="/" class="text-3xl font-serif font-bold tracking-tighter">H</a>
		
		<nav class="hidden lg:flex items-center gap-8 text-sm font-medium">
			<div class="group relative cursor-pointer flex items-center gap-1 hover:opacity-70 transition-opacity">
				Platform
				<svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:rotate-180"><path d="m6 9 6 6 6-6"/></svg>
			</div>
			<div class="group relative cursor-pointer flex items-center gap-1 hover:opacity-70 transition-opacity">
				Solutions
				<svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:rotate-180"><path d="m6 9 6 6 6-6"/></svg>
			</div>
			<a href="/customers" class="hover:opacity-70 transition-opacity">Customers</a>
			<a href="/security" class="hover:opacity-70 transition-opacity">Security</a>
			<div class="group relative cursor-pointer flex items-center gap-1 hover:opacity-70 transition-opacity">
				Resources
				<svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:rotate-180"><path d="m6 9 6 6 6-6"/></svg>
			</div>
			<div class="group relative cursor-pointer flex items-center gap-1 hover:opacity-70 transition-opacity">
				About
				<svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:rotate-180"><path d="m6 9 6 6 6-6"/></svg>
			</div>
		</nav>
	</div>

	<div class="flex items-center gap-6">
		<a href="/login" class="text-sm font-medium hover:opacity-70 transition-opacity">Login</a>
	</div>
</header>
