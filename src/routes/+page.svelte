<script>
	import Counter from './Counter.svelte';
	import Modal from './Modal.svelte'
	//  import question_icon from '$lib/images/question.png'
	let scuteCount = 1;
	let landCount = 0;
	let landsEntering = 1;
	let greenInsectCount = 0;

	let showModal = false;


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
	<h2>Don't want to do the maths on how many scutes you should have? look no further.</h2>


	<label for="lands">Current Lands</label>
	 <Counter bind:count={landCount} />
	<br/>
	<div><label for="lands-entering">Lands Entering Simultaneously</label>
	<span class='icon' onclick={() => (showModal = true)} >
		<enhanced:img src="../../static/question.png" alt="Image"/>
	</span>
	</div> 
	<br/>
	<Counter bind:count={landsEntering} />
	<br/>
	<input type="button"class="button-calculate" id="calculate" value="Calculate" onclick={calculate}>
	<br/>
	<label for="scute-count">Number of Scute Swarm</label>
	<br/>
	<Counter bind:count={scuteCount} />
	<br/>
	<label for="green-insect-token-count">Number of Green Insect Token</label>
	<br/>
	<Counter bind:count={greenInsectCount} />
	<br/>
	<p>Scute Damage: {(scuteCount)}</p>
	<p>Green Insect Damage: {(greenInsectCount)}</p>

	<input type="button" class="button-reset" value="Reset" onclick={reset}>

	{#snippet simultaneousLandExplanation()}
		<p>Cards with effects like <a href="https://scryfall.com/card/grn/125/circuitous-route">Circuitous Route</a> 
			cause the lands to enter at the same time. So only the scute swarms currently on the battlefield when the effect is played trigger and create copies for each land coming into play <br/><br/>
			If you have 2 scutes have 6 lands and play Circuitous Route, both scutes will trigger 2 times and you end with 6 scute swarm and 8 lands.
		</p>
	{/snippet}
	


	<Modal bind:showModal>
		{#snippet header()}
			<h3>Simultaneous lands entering</h3>
		{/snippet}
		
		{@render simultaneousLandExplanation()}

	</Modal>

</section>


<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	.button-calculate{
		background: #31da079a;
	}

	.button-reset{
		background: #ee1607ab;
	}

	h1 {
		width: 100%;
		/* margin-left: 1.2em; */
	}

	h2 {
		text-align: center;
		font-size: 1em;
	}

	.icon img {
	padding-left: 10px;
    height: 24px;
    width: 24px;
	display:inline-block
}
</style>