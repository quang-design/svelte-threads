<script lang="ts">
	import Logo from '$lib/assets/logo.svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import {
		House,
		Search,
		SquarePen,
		Heart,
		UserRound,
		Pin,
		Menu,
		Plus,
		type Icon as IconType
	} from '@lucide/svelte';
	import { page } from '$app/state';

	type NavItem = {
		name: string;
		href?: string;
		icon: typeof IconType;
	};

	const navItems: NavItem[] = [
		{
			name: 'Home',
			href: '/',
			icon: House
		},
		{
			name: 'Search',
			href: '/search',
			icon: Search
		},
		{
			name: 'Create',
			icon: SquarePen
		},
		{
			name: 'Activity',
			href: '/activity',
			icon: Heart
		},
		{
			name: 'Profile',
			href: '/profile',
			icon: UserRound
		}
	];

	let innerWidth = $state(0);

	// $inspect(innerWidth);
</script>

<svelte:window bind:innerWidth />

{#if innerWidth < 700}
	<!-- Mobile -->
	<header
		class="bg-background/85 fixed top-0 left-0 z-1 flex h-19 w-full flex-col items-center justify-center backdrop-blur-xl"
	>
		<div class="size-8">
			<a href="/" class="cursor-pointer touch-manipulation">
				<Logo />
			</a>
		</div>
		<div class="absolute top-5 right-5">
			<Button href="/login">Log in</Button>
		</div>
	</header>
	<nav
		class="bg-background/85 fixed right-0 bottom-0 left-0 z-1 grid h-14 grid-cols-5 grid-rows-1 items-center gap-1 p-1 backdrop-blur-xl"
	>
		{#each navItems as item}
			{@const Icon = item.icon}
			<Button href={item.href} variant="ghost" class="h-full">
				<Icon
					size={24}
					class={`scale-150 stroke-[2.25] ${page.url.pathname === item.href ? 'text-foreground' : 'text-gray-400'}`}
				/>
			</Button>
		{/each}
	</nav>
{:else if innerWidth < 1080}
	<!-- Tablet -->
	<nav
		class="bg-background/85 fixed top-0 bottom-0 left-0 z-1 flex h-full w-20 flex-col items-center gap-1 overflow-y-visible p-2 backdrop-blur-lg"
	>
		<div class="mt-1 flex h-8 shrink-0 justify-center">
			<a href="/" class="cursor-pointer touch-manipulation">
				<Logo />
			</a>
		</div>
		<div class="my-4 flex w-full grow flex-col justify-center gap-1 px-1">
			{#each navItems as item}
				{@const Icon = item.icon}
				{#if item.name === 'Create'}
					<Button variant="secondary" class="group h-11 cursor-pointer">
						<Plus
							size={24}
							class="group-hover:text-foreground scale-150 stroke-[2.25] text-gray-400"
						/>
					</Button>
				{:else}
					<Button href={item.href} variant="ghost" class="h-11">
						<Icon
							size={24}
							class={`scale-150 stroke-[2.25] ${page.url.pathname === item.href ? 'text-foreground' : 'text-gray-400'}`}
						/>
					</Button>
				{/if}
			{/each}
		</div>
		<div class="mb-5 flex h-fit w-full flex-col items-center gap-1 px-1">
			<Button variant="ghost" class="h-11 w-full cursor-pointer">
				<Pin size={24} class="scale-150 stroke-[2.25] text-gray-400" />
			</Button>
			<Button variant="link" class="group h-11 w-full cursor-pointer">
				<Menu size={24} class="group-hover:text-foreground scale-150 stroke-[2.25] text-gray-400" />
			</Button>
		</div>
	</nav>
	<div class="absolute top-5 right-5">
		<Button href="/login">Log in</Button>
	</div>
{:else}
	<!-- Desktop -->
	<nav
		class="bg-background/85 fixed top-0 bottom-0 left-0 z-1 flex h-full w-20 flex-col items-center gap-1 overflow-y-visible p-2 backdrop-blur-lg"
	>
		<div class="mt-1 flex h-8 shrink-0 justify-center">
			<a href="/" class="cursor-pointer touch-manipulation">
				<Logo />
			</a>
		</div>
		<div class="my-4 flex w-full grow flex-col justify-center gap-1 px-1">
			{#each navItems as item}
				{@const Icon = item.icon}
				{#if item.name === 'Create'}
					<Button
						variant="secondary"
						class="group h-11 cursor-pointer bg-gray-200 hover:bg-gray-200 hover:text-black"
					>
						<Plus
							size={24}
							class="group-hover:text-foreground scale-150 stroke-[2.25] text-gray-400"
						/>
					</Button>
				{:else}
					<Button href={item.href} variant="ghost" class="h-11">
						<Icon
							size={24}
							class={`scale-150 stroke-[2.25] ${page.url.pathname === item.href ? 'text-foreground' : 'text-gray-400'}`}
						/>
					</Button>
				{/if}
			{/each}
		</div>
		<div class="mb-5 flex h-fit w-full flex-col items-center gap-1 px-1">
			<Button variant="ghost" class="h-11 w-full cursor-pointer">
				<Pin size={24} class="scale-150 stroke-[2.25] text-gray-400" />
			</Button>
			<Button variant="link" class="group h-11 w-full cursor-pointer">
				<Menu size={24} class="group-hover:text-foreground scale-150 stroke-[2.25] text-gray-400" />
			</Button>
		</div>
	</nav>
{/if}
