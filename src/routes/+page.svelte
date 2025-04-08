
<section class="pt-36 lg:pt-8 hero flex h-full lg:min-h-dvh w-full flex-col lg:flex-row items-center justify-center">
	<div class="ttten absolute inset-0 z-0"></div>
    <div class="flex h-full w-full flex-col lg:flex-row items-center gap-8 justify-center z-20">
        <div class="flex h-full flex-col items-center lg:items-end justify-center gap-2 lg:gap-8">
            <h1 class="text-center lg:text-right">Protect Your Most <br> Valuable Asset</h1>
            <h2 class="opacity-85 text-center lg:text-right"><span class="opacity-80 ">Money doesn't rule the World.</span> <br><span class="italic">Time does</span></h2>
            <button class="glow mt-2 bg-primary hover:bg-secondary focus:bg-secondary active:bg-secondary rounded-md transition-all"><h4>Start using it in a better way</h4></button>
        </div>
        <div class="z-20 w-full max-w-md lg:max-w-xl">
            <img 
                src="/clockhero.png" 
                alt="Save Time With Automatization" 
                class="w-full h-auto object-contain lg:mt-12 opacity-90 hover:opacity-100 transition-all"
            >
        </div>
    </div>
</section>
<!-- 
<section class="what relative flex flex-col sm:flex-row h-full w-full items-center justify-center">
    <div class="bg-image absolute inset-0 z-0 h-full w-full"></div>
    <div class="flex gap-4 flex-col z-20">
        <h1 class="text-center">Don't do it all yourself</h1>
        <h2 class="opacity-70 text-center">Level up your business with Automation & AI</h2>
    
        <div class="flex gap-4 flex-col text-center">
            <h3>Get more done with less effort</h3>
            <h3>Automate repetitive tasks</h3>
            <h3>Optimize your workflows</h3>
        </div>
    </div>
</section> -->

<style>
	.hero {
		position: relative;
	}

    .ttten {
		background-image: linear-gradient(to bottom, transparent 0%, rgba(0, 0, 0, 0.87) 100%),url('/ttten.svg');
		background-position: center right;
		background-repeat: no-repeat;
		background-size: cover;
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		opacity: 0.3;
		z-index: 0;
	}
	.bg-image {
		background-image: linear-gradient(to top, transparent 0%, rgba(0, 0, 0, 0.845) 100%), url('/brillo.webp');
		background-position: bottom right;
		background-repeat: no-repeat;
		background-size: cover;
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		opacity: 0.8;
		z-index: 0;
	}
	/*
	.text-gradient {
		background: linear-gradient(to bottom, #fcdacf, #fcded4, #fce2d9, #fde5de, #fde9e2, #fef0ec);
		background-clip: text;
		color: transparent;
	}
		*/
</style>
