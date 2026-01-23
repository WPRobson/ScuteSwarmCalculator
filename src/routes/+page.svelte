<script>
	import Counter from './Counter.svelte';
	import Modal from './Modal.svelte';
	import { base } from '$app/paths'
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
	<title>Scute Swarm Calculator - MTG Token Counter Tool</title>
	<meta name="description" content="Free Scute Swarm Calculator for Magic: The Gathering. Accurately track your Scute Swarm tokens and Green Insect tokens during landfall triggers. Essential tool for MTG Commander and Standard players." />
	<meta name="keywords" content="Scute Swarm, MTG, Magic The Gathering, token calculator, landfall, Commander, EDH, Zendikar Rising" />
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

<section>
<br/>
<h3>Info</h3>
<p>This tool helps you determine the correct number of Scute Swarm tokens to create based on the number of lands entering the battlefield + existing Scute Swarm in play.</p>
<p>This site is designed to be used in conjunction with Magic: The Gathering games. To help players running the card "Scute Swarm" in their decks</p>
<h3>Usage</h3>
<p>1. Set the current number of lands you have in play</p>
<p>2. Set the number of lands entering the battlefield simultaneously</p>
<p>3. Click Calculate. The number of Scute Swarm and Green Insect tokens will be updated accordingly</p>
<p>4. If needed, Number of Scute Swarm tokens and insect tokens can be adjusted manually</p>
<p>5. Click Reset to start over</p>
<h3>Lands Entering Simultaneously</h3>
<p>Cards with effects like <a href="https://scryfall.com/card/grn/125/circuitous-route">Circuitous Route</a> 
	cause the lands to enter at the same time. So only the scute swarms currently on the battlefield when the effect is played trigger and create copies for each land coming into play <br/><br/>
	If you have 2 scutes have 6 lands and play Circuitous Route, both scutes will trigger 2 times and you end with 6 scute swarm and 8 lands.
</p>
</section>

<section class="faq-section">
	<h3>Frequently Asked Questions</h3>
	
	<details>
		<summary>What is Scute Swarm?</summary>
		<p>Scute Swarm is a creature card from Magic: The Gathering's Zendikar Rising set. It's a 1/1 green Insect with a landfall ability that creates tokens whenever a land enters the battlefield under your control. Below 6 lands, it creates 1/1 Insect tokens. At 6+ lands, it creates copies of itself, leading to exponential growth.</p>
	</details>

	<details>
		<summary>Why do I need a calculator for Scute Swarm?</summary>
		<p>Once you have 6 or more lands, each land causes every Scute Swarm to copy itself. This exponential growth can quickly result in hundreds or thousands of tokens, making manual counting impractical and error-prone during gameplay.</p>
	</details>

	<details>
		<summary>How does the landfall trigger work?</summary>
		<p>Landfall triggers whenever a land enters the battlefield under your control. If you have multiple Scute Swarms, each one triggers separately. If multiple lands enter simultaneously (like with Cultivate), each Scute Swarm triggers once for each land, using the number of Scutes present when the ability resolves.</p>
	</details>

	<details>
		<summary>What's the difference between Scute Swarm tokens and Green Insect tokens?</summary>
		<p>Before you reach 6 lands, Scute Swarm creates generic 1/1 green Insect creature tokens. At 6+ lands, it creates token copies of Scute Swarm itself, which also have the landfall ability and will continue to multiply with future land drops.</p>
	</details>

	<details>
		<summary>Can I use this calculator during tournament play?</summary>
		<p>Yes! Using external tools to track game state (like token counts) is generally allowed in Magic tournaments. However, always check with the head judge if you're unsure. The calculator helps ensure accurate counts, which benefits both players.</p>
	</details>

	<details>
		<summary>What cards work well with Scute Swarm?</summary>
		<p>Cards that put multiple lands into play simultaneously are excellent: Cultivate, Kodama's Reach, Circuitous Route, and Boundless Realms. Fetch lands also work great since they trigger landfall twice. Check out our <a href="{base}/guide">Strategy Guide</a> for comprehensive combo information.</p>
	</details>
</section>

<section class="learn-more">
	<h3>Learn More About Scute Swarm</h3>
	<p>Want to master Scute Swarm strategies and build the ultimate landfall deck? Check out our comprehensive resources:</p>
	<div class="link-cards">
		<a href="{base}/guide" class="link-card">
			<h4>📖 Strategy Guide</h4>
			<p>Learn combos, deck building tips, and advanced play patterns</p>
		</a>
		<a href="{base}/about" class="link-card">
			<h4>ℹ️ About This Tool</h4>
			<p>Why we built this calculator and how it helps MTG players</p>
		</a>
	</div>
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

	/* FAQ Section Styles */
	.faq-section {
		max-width: 700px;
		margin: 2rem auto;
		padding: 1rem;
	}

	.faq-section h3 {
		text-align: center;
		color: #2e7d32;
		margin-bottom: 1.5rem;
	}

	details {
		background: #f5f5f5;
		border-radius: 8px;
		margin-bottom: 0.75rem;
		padding: 0;
		border: 1px solid #e0e0e0;
	}

	summary {
		padding: 1rem 1.25rem;
		cursor: pointer;
		font-weight: 600;
		color: #333;
		list-style: none;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	summary::-webkit-details-marker {
		display: none;
	}

	summary::after {
		content: '+';
		font-size: 1.25rem;
		color: #4caf50;
	}

	details[open] summary::after {
		content: '−';
	}

	details p {
		padding: 0 1.25rem 1rem;
		margin: 0;
		color: #555;
		line-height: 1.6;
	}

	details a {
		color: #1976d2;
	}

	/* Learn More Section */
	.learn-more {
		max-width: 700px;
		margin: 2rem auto;
		padding: 2rem 1rem;
		text-align: center;
	}

	.learn-more h3 {
		color: #2e7d32;
		margin-bottom: 1rem;
	}

	.learn-more > p {
		color: #555;
		margin-bottom: 1.5rem;
	}

	.link-cards {
		display: flex;
		gap: 1rem;
		justify-content: center;
		flex-wrap: wrap;
	}

	.link-card {
		background: #e8f5e9;
		border: 2px solid #81c784;
		border-radius: 12px;
		padding: 1.5rem;
		text-decoration: none;
		color: inherit;
		flex: 1;
		min-width: 200px;
		max-width: 280px;
		transition: transform 0.2s, box-shadow 0.2s;
	}

	.link-card:hover {
		transform: translateY(-2px);
		box-shadow: 0 4px 12px rgba(0,0,0,0.15);
	}

	.link-card h4 {
		color: #2e7d32;
		margin: 0 0 0.5rem 0;
		font-size: 1.1rem;
	}

	.link-card p {
		margin: 0;
		color: #555;
		font-size: 0.9rem;
	}
</style>