<script>
	import SearchBar from "../components/SearchBar/SearchBar.svelte";
	import PromoCard from "../components/PromoCard.svelte";

	const promos = [
		{
			title: "20% Off",
			description: "Get 20% off on all cocktails, 24/7",
			outlet: "Starbucks Dewata"
		},
		{
			title: "Buy 2 Get 1",
			description: "On all appetizers and desserts",
			outlet: "House of Waffles"
		}
	]
</script>

<style>
	.list {
		padding: 0 24px;
	}
</style>

<svelte:head>
	<title>Ciplah</title>
</svelte:head>

<SearchBar/>

<div class="list">
	{#each promos as promo}
	<PromoCard promo={promo}/>
	{/each}
</div>
