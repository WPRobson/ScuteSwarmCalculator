<script>
	import Counter from './Counter.svelte';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import scute_swarm from '$lib/images/scute_swarm.jpg';
	let scuteCount = 1;
	let landCount = 0;
	let landsEntering = 1;
	let greenInsectCount = 0;


	function calculate(){
		landCount = landCount += landsEntering
		if (landCount <6) {
			greenInsectCount += scuteCount
		}else{
			scuteCount = (scuteCount) * (landsEntering+1)
		}
		landsEntering = 1;
	}

	function reset(){
		scuteCount = 1;
		greenInsectCount = 0;
		landCount = 0;
		landsEntering = 1;
	}

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Scute Swarm Calculator" />
</svelte:head>

<section>
	<h1 class="card-name">Scute Swarm Calculator</h1>
	<h2>Do you not want to do the maths on how many scutes you should have? look no further.</h2>

	<br/>
	<input type="button" value="reset" on:click={reset}>
	<br/>
	<label for="lands">Current Lands</label>
	 <Counter bind:count={landCount} />
	<br/>
	<label for="lands-entering">Lands Entering Simultaneously</label>
	<br/>
	<Counter bind:count={landsEntering} />
	<br/>
	<input type="button" id="calculate" value="Calculate" on:click={calculate}>
	<br/>
	<label for="scute-count">Number of Scute Swarm</label>
	<br/>
	<Counter bind:count={scuteCount} />
	<br/>
	<label for="green-insect-token-count">Number of Green Insect Token</label>
	<br/>
	<Counter bind:count={greenInsectCount} />
	<br/>
	<p>Scute Damage: {(scuteCount)*1}</p>
	<p>Green Insect Damage: {(greenInsectCount)*1}</p>

</section>


<style>

	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	/* h1.card-name{
		
	} */

	h1 {
		width: 100%;
		margin-left: 1.2em;
	}

	h2 {
		text-align: center;
		font-size: 1em;
	}

	/* .welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}



	.welcome img {
		position: absolute;
		width: 50%;
		height: 100%;
		top: 0;
		display: block;
	} */
</style>