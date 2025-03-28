<script lang="ts">
	import { page } from '$app/state';
	import { fade } from 'svelte/transition';

	const items = [
		{ label: 'Contact', href: '/contact' },
		{ label: 'About', href: '/about' }
	];

	let isMobileMenuOpen = $state(false);

	// Prevent scrolling when menu is open
	$effect(() => {
		if (isMobileMenuOpen) {
			document.body.style.overflow = 'hidden';
		} else {
			document.body.style.overflow = 'unset';
		}
	});
</script>

<div class="@container fixed top-6 z-50 flex w-full items-center justify-center self-center">
	<div
		class="glow flex w-fit flex-row items-center justify-between gap-2 rounded-full border bg-background/70 px-6 sm:gap-12"
	>
		<a href="/" class="group flex flex-row items-center justify-center">
			<img src="/personalFlow.svg" alt="Personal Flow" class="size-16" />
			<h4 class="title-gradient transition-all group-hover:text-primary/75">PersonalFlow</h4>
		</a>

		<!-- Desktop Navigation -->
		<nav class="hidden sm:block">
			<ul class="flex flex-row gap-4">
				{#each items as { href, label }}
					<li>
						<a
							{href}
							class="opacity-75 hover:opacity-100 {page.url.pathname === href
								? 'font-semibold text-primary'
								: ''}"
						>
							{label}
						</a>
					</li>
				{/each}
			</ul>
		</nav>

		<!-- Mobile Navigation Trigger -->
		<button
			class="sm:hidden"
			aria-label="Open Menu"
			aria-expanded={isMobileMenuOpen}
			onclick={() => (isMobileMenuOpen = !isMobileMenuOpen)}
		>
			<img
				src="/icons/burger.svg"
				alt="Menu"
				class="size-6 opacity-80 invert hover:opacity-100 active:opacity-100"
			/>
		</button>
	</div>

	<!-- Mobile Menu Overlay -->
	{#if isMobileMenuOpen}
		<div
			transition:fade={{ duration: 200 }}
			class="fixed inset-0 z-40 flex flex-col items-center justify-center bg-background/90 backdrop-blur-lg"
		>
			<button
				aria-label="Close Menu"
				class="absolute right-6 top-6"
				onclick={() => (isMobileMenuOpen = false)}
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="size-8"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M6 18L18 6M6 6l12 12"
					/>
				</svg>
			</button>

			<nav class="flex flex-col items-center justify-center space-y-8">
				<a href="/" class="group flex flex-row items-center justify-center">
					<img src="/personalFlow.svg" alt="Personal Flow" class="size-24" />
					<h4 class="title-gradient text-3xl font-bold transition-all group-hover:text-primary/75">
						PersonalFlow
					</h4>
				</a>

				<ul class="flex flex-col items-center gap-6">
					{#each items as { href, label }}
						<li>
							<a
								{href}
								class="text-2xl opacity-75 hover:opacity-100 {page.url.pathname === href
									? 'font-semibold text-primary'
									: ''}"
								onclick={() => (isMobileMenuOpen = false)}
							>
								{label}
							</a>
						</li>
					{/each}
				</ul>
			</nav>
		</div>
	{/if}
</div>

<style>
	/* Add any additional styling here if needed */
</style>
