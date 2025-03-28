
<section class="hero relative flex h-dvh w-full flex-col items-center justify-center">
	<div class="bg-image absolute inset-0 z-0"></div>
	<div class="flex h-full w-full flex-col items-center justify-center z-20 gap-8">
		<h1 class="text-gradient text-center">Protect Your Most <br> Valuable Asset</h1>
        <h2 class="opacity-70 text-center"><span class="opacity-60 ">Money doesn't rule the World.</span> <br><span class="italic">Time does</span></h2>
        <button class="glow mt-2 bg-primary hover:bg-secondary focus:bg-secondary active:bg-secondary rounded-full transition-all"><h4>Start using it in a better way</h4></button>
    </div>
</section>

<section class="newsletter flex flex-col">
    <div class="flex-col">
        <h1 class="text-gradient text-center">What we do?</h1>
    </div>
    <div class="div">

    </div>
</section>

<style>
	.hero {
		position: relative;
		overflow: hidden;
	}

	.bg-image {
		background-image: linear-gradient(to bottom, transparent 0%, black 100%), url('/brillo.webp');
		background-position: right;
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

	.text-gradient {
		background: linear-gradient(to bottom, #fcdacf, #fcded4, #fce2d9, #fde5de, #fde9e2, #fef0ec);
		background-clip: text;
		color: transparent;
	}
</style>
