<script lang="ts">
	import Logo from '$lib/assets/logo.svelte';
</script>

<nav
	class="fixed top-0 left-0 z-1 flex h-full w-20 flex-col items-center bg-white/85 backdrop-blur-lg"
>
	<div class="flex shrink-0 justify-center overflow-hidden py-4">
		<a
			href="/"
			class="relative block size-9 min-h-0 basis-auto cursor-pointer touch-manipulation rounded-[inherit] border-0 select-none"
		>
			<Logo className="hover:scale-105 duration-200" />
		</a>
	</div>
</nav>
