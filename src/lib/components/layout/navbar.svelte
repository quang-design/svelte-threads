<script lang="ts">
	import Logo from '$lib/assets/logo.svelte';
	import { Heart, House, Menu, Plus, Search, User } from '@lucide/svelte';
</script>

<!-- Navbar Med-->
<nav
	class="fixed top-0 left-0 z-1 flex h-full w-19 flex-col items-center justify-between bg-gray-100/85 p-1 backdrop-blur-lg"
>
	<!-- Logo -->
	<div class="flex shrink-0 justify-center overflow-hidden py-2">
		<a
			href="/"
			class="relative block size-9 min-h-0 basis-auto touch-manipulation rounded-[inherit] border-0 select-none"
		>
			<Logo className="hover:scale-105 duration-200" />
		</a>
	</div>
	<!-- Navigation -->
	<div class="flex w-full grow flex-col justify-center gap-1">
		{@render navItem('/', House, true)}
		{@render navItem('/search', Search, false)}
		{@render navItem('/create', Plus, false, true, 'group-hover:stroke-black')}
		{@render navItem('/activity', Heart, false)}
		{@render navItem('/profile', User, false)}
	</div>
	<!-- Menu -->
	<div class="mb-5 flex shrink-0 cursor-pointer justify-center overflow-hidden py-2">
		<Menu size="26" class="relative shrink-0 stroke-gray-400 stroke-2 hover:stroke-black" />
	</div>
</nav>

{#snippet navItem(href = '/', icon = House, active = false, highlight = false, iconClass = '')}
	<div class="relative">
		<a
			{href}
			class="group relative z-0 m-0 flex cursor-pointer touch-manipulation rounded-2xl border-0 p-1"
		>
			<div class="flex w-full items-center justify-center py-3 duration-200 ease-in-out">
				<div
					class={highlight
						? 'absolute top-0 z-0 mt-1 mb-1 h-[calc(100%-6px)] w-full scale-[0.85] rounded-2xl bg-gray-200 transition-all duration-100 ease-out'
						: 'absolute top-0 z-0 mt-1 mb-1 h-[calc(100%-6px)] w-full scale-[0.5] rounded-2xl bg-gray-200 opacity-0 transition-all duration-100 ease-out group-hover:scale-[0.85] group-hover:opacity-100'}
				></div>
				<div>
					<svelte:component
						this={icon}
						size={26}
						class={`relative shrink-0 stroke-2 ${active ? ' stroke-black' : `stroke-gray-400 ${iconClass}`}`}
					/>
				</div>
			</div>
		</a>
	</div>
{/snippet}
