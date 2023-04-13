<script>
	import {onMount} from 'svelte';
	import Square from "./Square.svelte";
	
	let card = ["placeholder"];
	let squares = [
		"Sonic",
		"Ashley Burch",
		"Return of the P*ussy Wag*on",
		"Hero and Taylor flirt",
		"Scary is an anchor",
		"Normal casts revivify",
		"Scam likely appearance",
		"Taylor Swift reference",
		"Scary references the fact that her dad left",
		"Freddie makes a Disney reference",
		"Taylor weebs",
		"Well... Well... Well...",
		"Jimmy Wong",
		"A teen says they don't care",
		"Willie is abusive towards Scary",
		"Link references his life in a simulation",
		"Normal has 2 dads",
		"A reference to IRL Beth May",
		"Mr. Mustache appears",
		"Link insults Hermy",
		"Cats come from the good plane",
		"Ron is in the Goofs Plane",
		"Scary says her stomach hurts",
		"Urine"
	];
	
	function create() {
		let working = squares;
		card = [];
		while(working.length>0) {
			let num = Math.round(Math.random()*(working.length-1));
			card.push(working[num]);
			working.splice(num, 1);
		}
		card.splice(12, 0, "Free Space");
		console.log(card);
	}
	
	
	onMount(async () => {
		create();
	});
</script>
<div class="main">
	{#each card as square}
		<Square text={square}></Square>
	{/each}
</div>
<style>
	.main {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		width: 500px;
		max-width: 500px;
		min-width: 500px;
		height: 500px;
		max-width: 500px;
		min-width: 500px;
	}
</style>