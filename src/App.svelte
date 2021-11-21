<script>
	import Prev from "./Prev.svelte";
	import Card from "./Card.svelte";
	import Next from "./Next.svelte";
	import "tailwindcss/tailwind.css";
	let arr = [1,2,3,4,5];
</script>

<main class="container w-screen">
	<div class="p-16 flex justify-between">
		<h1 class="text-3xl font-sans font-bold text-gray-800">Projects based on your profile</h1>
		<a href="smth" class="text-2xl font-sans font-bold text-gray-800 underline">View all projects</a>
	</div>
	<div class="flex">
		<Prev />
		<div class="overflow-x-hidden slide_wrapper">
			<div class="flex wrapper">
				{#each arr as item}
    		<Card />
  			{/each}
			</div>
		</div>
		<Next />
	</div>
</main>

<style>
</style>