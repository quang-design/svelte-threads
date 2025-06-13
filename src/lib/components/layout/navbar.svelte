<script lang="ts">
	import Logo from '$lib/assets/logo.svelte';
	import { Button } from '$lib/components/ui/button/index.js';
</script>

<header
	class="bg-background fixed top-0 left-0 z-1 flex h-19 w-full flex-col items-center justify-center backdrop-blur-xl"
>
	<div class="size-8">
		<a href="/" class=" flex cursor-pointer touch-manipulation">
			<Logo />
		</a>
	</div>
	<div class="absolute top-5 right-5">
		<Button href="/login">Log in</Button>
	</div>
</header>
