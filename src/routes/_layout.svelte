<script lang="ts">
	import Tailwindcss from '../components/Tailwindcss.svelte';
	import Nav from '../components/Nav.svelte';

	export let segment: string;
</script>

<style>
	main {
		position: relative;
		max-width: 56em;
		background-color: white;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>

<Tailwindcss />

<Nav {segment}/>

<main class="w-screen flex flex-wrap text-center">
	<slot></slot>
</main>