<script>
	import { Button } from '$lib/components/ui/button/index.js';
</script>

<div
	class="sticky top-16 mt-16 flex h-fit w-xs flex-col items-center gap-2 rounded-3xl border-[0.5px] border-gray-300 p-6"
>
	<h2 class="text-center text-xl font-bold">Log in or sign up for Threads</h2>
	<p class="text-center text-sm text-gray-400">
		See what people are talking about and join the conversation.
	</p>
	<Button href="/login" variant="default" class="mt-4 w-full">Log in</Button>
	<Button href="/signup" variant="link" class="mt-2 w-full">Login with username instead</Button>
</div>
