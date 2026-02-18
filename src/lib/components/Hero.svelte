<style>
    /* Animation keyframes */
    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(20px);
            filter: blur(4px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
            filter: blur(0);
        }
    }

    @keyframes fadeIn {
        from { opacity: 0; }
        to { opacity: 1; }
    }

    @keyframes scaleIn {
        from {
            opacity: 0;
            transform: scale(0.95);
        }
        to {
            opacity: 1;
            transform: scale(1);
        }
    }

    /* Base animation class */
    .animate-fade-in-up {
        opacity: 0;
        animation: fadeInUp 0.8s cubic-bezier(0.22, 0.61, 0.36, 1) forwards;
    }

    .animate-fade-in {
        opacity: 0;
        animation: fadeIn 0.8s cubic-bezier(0.22, 0.61, 0.36, 1) forwards;
    }

    .animate-scale-in {
        opacity: 0;
        animation: scaleIn 0.8s cubic-bezier(0.22, 0.61, 0.36, 1) forwards;
    }

    /* Staggered delays */
    .delay-200 { animation-delay: 200ms; }
    .delay-300 { animation-delay: 300ms; }
    .delay-400 { animation-delay: 400ms; }
    .delay-700 { animation-delay: 700ms; }

    /* Custom scrollbar hiding */
    .no-scrollbar::-webkit-scrollbar {
        display: none;
    }
    .no-scrollbar {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }
</style>

<section class="relative h-screen flex flex-col justify-center text-white overflow-hidden">
	<!-- Background Image -->
	<div class="absolute inset-0 z-0">
		<img 
			src="/generated/image-a-dark-sophisticated-high-end-corporate--1771432385567-0.webp" 
			alt="Background" 
			class="w-full h-full object-cover animate-scale-in duration-[1.5s]"
		/>
		<div class="absolute inset-0 bg-gradient-to-r from-black/90 via-black/60 to-black/30 z-10"></div>
        <div class="absolute inset-0 bg-gradient-to-t from-black via-transparent to-black/40 z-10"></div>
	</div>

	<!-- Content -->
	<div class="relative z-40 container mx-auto px-6 md:px-10 max-w-[1400px] w-full">
		<div class="max-w-4xl">
			<h1 class="text-balance font-serif text-5xl sm:text-6xl md:text-7xl lg:text-[5.5rem] leading-[1.1] tracking-tight text-white mb-6 animate-fade-in-up delay-200">
				Investor-Grade Diligence in Days
			</h1>
			<p class="text-pretty text-lg md:text-xl text-gray-200 leading-relaxed max-w-2xl mb-10 font-light animate-fade-in-up delay-300">
				Private equity deal teams trust DiligenceSquared to deliver institutional-grade market intelligence through AI-moderated expert interviews.
			</p>
			<div class="animate-fade-in-up delay-400">
				<a href="#" class="inline-block bg-white text-black text-sm md:text-base font-semibold py-3 px-8 rounded-sm hover:bg-gray-100 transition-colors duration-200">
					Book a Demo
				</a>
			</div>
		</div>
	</div>

	<!-- Bottom Bar -->
	<footer class="absolute bottom-0 left-0 w-full z-40 border-t border-white/10 bg-gradient-to-t from-black/90 to-transparent backdrop-blur-[2px] animate-fade-in delay-700">
        <div class="flex flex-col md:flex-row items-center justify-between px-6 md:px-10 py-6 md:py-8 gap-6">
            
            <!-- Logos Container -->
            <div class="w-full md:w-auto overflow-x-auto no-scrollbar">
                <div class="flex items-center gap-8 md:gap-12 min-w-max opacity-70 grayscale hover:grayscale-0 hover:opacity-100 transition-all duration-500">
                    <span class="font-serif tracking-wide">Ewater</span>
                    <span class="font-serif tracking-wide">Macfarlanes</span>
                    <span class="font-bold tracking-tighter">KKR</span>
                    <span class="font-bold tracking-wide">A&O SHEARMAN</span>
                    <span class="font-serif tracking-wide">Gleiss Lutz</span>
                    <span class="font-bold tracking-tighter">CMS</span>
                    <span class="uppercase tracking-widest text-xs font-bold">Cuatrecasas</span>
                    <div class="flex flex-col leading-none">
                        <span class="font-serif italic text-sm">Thompson</span>
                        <span class="font-serif text-xs uppercase tracking-widest">Hine</span>
                    </div>
                    <span class="font-bold tracking-wide">MERCK</span>
                </div>
            </div>

            <!-- Customers Button -->
            <div class="flex-shrink-0 hidden md:block">
                <a href="#" class="inline-flex items-center justify-center border border-white/30 rounded-sm px-4 py-2 text-xs uppercase tracking-wider font-medium text-white hover:bg-white/10 transition-colors">
                    Our Customers
                </a>
            </div>
        </div>
    </footer>
</section>
