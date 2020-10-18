<script>
	// import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	:global(body) {
		background-color: rgba(10, 20, 30, .1);
	}

	main {
		max-width: 100vw;
		min-height: 100vh;
		overflow-x: hidden;
	}
</style>

<!--<Nav {segment}/>-->

<main>
	<slot></slot>
</main>
