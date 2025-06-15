<script lang="ts">
	import '../app.css';
	import Navbar from '$lib/components/layout/navbar.svelte';
	import Login from '$lib/components/layout/login.svelte';

	let { children } = $props();

	let innerWidth = $state(0);
</script>

<svelte:window bind:innerWidth />

<main class="mx-auto ml-6 flex min-h-screen w-full justify-center gap-3 px-3">
	<Navbar />
	{@render children()}
	{#if innerWidth > 1080}
		<Login />
	{/if}
</main>
