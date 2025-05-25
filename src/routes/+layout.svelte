<script lang="ts">
	import '../app.css';
	import { Toaster } from 'svelte-sonner';
	import { afterNavigate, beforeNavigate } from '$app/navigation';

	let { children } = $props();

	beforeNavigate(() => {
		document.documentElement.style.scrollBehavior = 'auto';
	});

	afterNavigate((nav) => {
		if (!nav.from) return;
		window.scrollTo(0, 0);
		document.documentElement.style.scrollBehavior = '';
	});
</script>

{@render children()}
<Toaster />
