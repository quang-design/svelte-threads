<script lang="ts">
	import Logo from '$lib/assets/logo.svelte';
	import { Equal, Heart, House, Menu, Plus, Search, User } from '@lucide/svelte';
</script>

<nav
	class="fixed top-0 left-0 z-1 flex h-full w-19 flex-col items-center justify-between bg-gray-50/85 p-1 backdrop-blur-lg"
>
	<div class="flex shrink-0 justify-center overflow-hidden py-4">
		<a
			href="/"
			class="relative block size-9 min-h-0 basis-auto touch-manipulation rounded-[inherit] border-0 select-none"
		>
			<Logo className="hover:scale-105 duration-200" />
		</a>
	</div>
	<div class="flex w-full grow flex-col justify-center gap-1">
		<div class="relative">
			<a
				href="/"
				class="group relative z-0 m-0 flex cursor-pointer touch-manipulation rounded-2xl border-0 p-1"
			>
				<div class="flex h-12 w-16 items-center justify-center duration-200 ease-in-out">
					<div
						class="absolute top-0 z-0 mt-1 mb-1 h-[calc(100%-6px)] w-full scale-[0.5] rounded-2xl bg-gray-100 opacity-0 transition-all duration-100 ease-out group-hover:scale-[0.85] group-hover:opacity-100"
					></div>
					<div>
						<House size="26" class="relative shrink-0 stroke-2" />
					</div>
				</div>
			</a>
		</div>
		<div class="relative">
			<a
				href="/"
				class="group relative z-0 m-0 flex cursor-pointer touch-manipulation rounded-2xl border-0 p-1"
			>
				<div class="flex h-12 w-16 items-center justify-center duration-200 ease-in-out">
					<div
						class="absolute top-0 z-0 mt-1 mb-1 h-[calc(100%-6px)] w-full scale-[0.5] rounded-2xl bg-gray-100 opacity-0 transition-all duration-100 ease-out group-hover:scale-[0.85] group-hover:opacity-100"
					></div>
					<div>
						<Search size="26" class="relative shrink-0 stroke-gray-400 stroke-2" />
					</div>
				</div>
			</a>
		</div>
		<div class="relative">
			<a
				href="/"
				class="group relative z-0 m-0 flex cursor-pointer touch-manipulation rounded-2xl border-0 p-1"
			>
				<div class="flex h-12 w-16 items-center justify-center duration-200 ease-in-out">
					<div
						class="absolute top-0 z-0 mt-1 mb-1 h-[calc(100%-6px)] w-full scale-[0.85] rounded-2xl bg-gray-100 transition-all duration-100 ease-out"
					></div>
					<div>
						<Plus
							size="26"
							class="relative shrink-0 stroke-gray-400 stroke-2 group-hover:stroke-black"
						/>
					</div>
				</div>
			</a>
		</div>
		<div class="relative">
			<a
				href="/"
				class="group relative z-0 m-0 flex cursor-pointer touch-manipulation rounded-2xl border-0 p-1"
			>
				<div class="flex h-12 w-16 items-center justify-center duration-200 ease-in-out">
					<div
						class="absolute top-0 z-0 mt-1 mb-1 h-[calc(100%-6px)] w-full scale-[0.5] rounded-2xl bg-gray-100 opacity-0 transition-all duration-100 ease-out group-hover:scale-[0.85] group-hover:opacity-100"
					></div>
					<div>
						<Heart size="26" class="relative shrink-0 stroke-gray-400 stroke-2" />
					</div>
				</div>
			</a>
		</div>
		<div class="relative">
			<a
				href="/"
				class="group relative z-0 m-0 flex cursor-pointer touch-manipulation rounded-2xl border-0 p-1"
			>
				<div class="flex h-12 w-16 items-center justify-center duration-200 ease-in-out">
					<div
						class="absolute top-0 z-0 mt-1 mb-1 h-[calc(100%-6px)] w-full scale-[0.5] rounded-2xl bg-gray-100 opacity-0 transition-all duration-100 ease-out group-hover:scale-[0.85] group-hover:opacity-100"
					></div>
					<div>
						<User size="26" class="relative shrink-0 stroke-gray-400 stroke-2" />
					</div>
				</div>
			</a>
		</div>
	</div>
	<div class="flex shrink-0 cursor-pointer justify-center overflow-hidden py-4">
		<Equal size="26" class="relative shrink-0 stroke-gray-400 stroke-2 hover:stroke-black" />
	</div>
</nav>
