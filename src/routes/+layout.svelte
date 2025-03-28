<script lang="ts">
	import { ModeWatcher } from 'mode-watcher';
	import '../app.css';
	import Header from '$lib/components/Header.svelte';
	import ScreenSize from '$lib/components/ScreenSize.svelte';
	let { children } = $props();
</script>
<div class="h-full w-full relative">
	<ModeWatcher defaultMode="dark" />
	<Header />
	{@render children()}
</div>

<ScreenSize/>
