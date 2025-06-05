<script lang="ts">
	import '../app.css';
	import Navbar from '$lib/components/layout/navbar.svelte';

	let { children } = $props();
</script>

<Navbar />
<main class="min-h-screen p-4">
	{@render children()}
</main>
