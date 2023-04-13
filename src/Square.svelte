<script>
	let clicked = false;
	export let text = "";
	
	function handleClick() {
		if(clicked) {
			clicked=false;
		} else {
			clicked=true;
		}
	}
</script>
<div class="main">
	{#if clicked}
		<button style="background-color: green;" on:click={handleClick}>
			{text}
		</button>
	{:else}
		<button on:click={handleClick}>
			{text}
		</button>
	{/if}
</div>
<style>
	button {
		height: 100px;
		min-height: 100px;
		max-height: 100px;
		width: 100px;
		min-width: 100px;
		max-width: 100px;
	}
	@media (max-width: 800px) {
		button {
			height: 55px;
			min-height: 55px;
			max-height: 55px;
			width: 55px;
			min-width: 55px;
			max-width: 55px;
			font-size: 0.4em;
		}
	}
</style>
