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
			height: 50px;
			min-height: 50px;
			max-height: 50px;
			width: 50px;
			min-width: 50px;
			max-width: 50px;
			font-size: 0.5em;
		}
	}
</style>
