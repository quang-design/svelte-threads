<script lang="ts">
	import '../app.css';
	import Navbar from '$lib/components/layout/navbar.svelte';
	import Login from '$lib/components/layout/login.svelte';

	let { children } = $props();

	let innerWidth = $state(0);
</script>

<svelte:window bind:innerWidth />

<Navbar />
<main class="mx-auto flex min-h-screen justify-center gap-3 sm:px-5">
	{@render children()}
	{#if innerWidth > 1080}
		<Login />
	{/if}
</main>
