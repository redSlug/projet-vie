<script>
	import StubCard from './StubCard.svelte';

	let { items = [], path } = $props();

</script>

<article id="portfolio" class="panel">
	<!-- <LayoutGrid> -->
	<div id="wrapper">
		{#each items as item}
			<div class="cell">
				<StubCard {path} {item} width={"100px"} height={""}/>
			</div>
		{/each}
	</div>
	<!-- </LayoutGrid> -->
</article>

<style>
	.cell {
	  display: flex;
	  justify-content: center;
	  align-items: center;
	  color: var(--mdc-theme-on-secondary, #fff);
	}

	#wrapper {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		row-gap: 50px;
		column-gap: 25px;
	}
</style>
