<script>
</script>

<svelte:head>
	<title>About - Scute Swarm Calculator</title>
	<meta name="description" content="Learn about the Scute Swarm Calculator tool and why it was created for Magic: The Gathering players." />
</svelte:head>

<article>
	<h1>About Scute Swarm Calculator</h1>
	
	<section>
		<h2>Why We Built This Tool</h2>
		<p>
			If you've ever played Magic: The Gathering with a <strong>Scute Swarm</strong> deck, you know the chaos that ensues 
			once you hit six lands. What starts as a single 1/1 creature quickly spirals into dozens, hundreds, or even 
			thousands of tokens—and keeping track of them all can bring your game to a grinding halt.
		</p>
		<p>
			The Scute Swarm Calculator was created to solve this exact problem. Instead of fumbling with dice, pen and paper, 
			or mental math during intense games, you can quickly and accurately determine exactly how many Scute Swarm copies 
			and Green Insect tokens you should have on the battlefield.
		</p>
	</section>

	<section>
		<h2>Understanding Scute Swarm</h2>
		<p>
			<strong>Scute Swarm</strong> is a creature card from the Zendikar Rising expansion (2020). It's a 1/1 green Insect 
			with a landfall ability that reads:
		</p>
		<blockquote>
			<em>"Whenever a land enters the battlefield under your control, create a 1/1 green Insect creature token. 
			If you control six or more lands, create a token that's a copy of Scute Swarm instead."</em>
		</blockquote>
		<p>
			This seemingly simple ability creates exponential growth once you reach six lands. Each land drop doesn't just 
			create one token—it causes every Scute Swarm you control to create a copy of itself, leading to explosive 
			board states.
		</p>
	</section>

	<section>
		<h2>The Math Behind the Madness</h2>
		<p>
			Let's break down how Scute Swarm multiplication works:
		</p>
		<ul>
			<li><strong>Lands 1-5:</strong> Each land creates 1/1 green Insect tokens (linear growth)</li>
			<li><strong>Land 6+:</strong> Each land doubles your Scute Swarm count (exponential growth)</li>
		</ul>
		<p>
			For example, if you have 1 Scute Swarm and 5 lands, then play your 6th land:
		</p>
		<ul>
			<li>Land 6: 1 Scute → 2 Scutes</li>
			<li>Land 7: 2 Scutes → 4 Scutes</li>
			<li>Land 8: 4 Scutes → 8 Scutes</li>
			<li>Land 9: 8 Scutes → 16 Scutes</li>
			<li>Land 10: 16 Scutes → 32 Scutes</li>
		</ul>
		<p>
			But it gets more complex when multiple lands enter simultaneously through cards like 
			<a href="https://scryfall.com/card/grn/125/circuitous-route" target="_blank" rel="noopener">Circuitous Route</a> or 
			<a href="https://scryfall.com/card/cmr/243/kodamas-reach" target="_blank" rel="noopener">Kodama's Reach</a>. 
			Our calculator handles these scenarios accurately.
		</p>
	</section>

	<section>
		<h2>Who Is This For?</h2>
		<p>
			This tool is perfect for:
		</p>
		<ul>
			<li><strong>Commander/EDH Players</strong> - Where Scute Swarm is a popular win condition in landfall decks</li>
			<li><strong>Standard & Pioneer Players</strong> - Running Scute Swarm in competitive formats</li>
			<li><strong>Kitchen Table Magic</strong> - Casual games where Scute Swarm shenanigans are encouraged</li>
			<li><strong>MTG Arena Players</strong> - While Arena tracks tokens automatically, this helps you plan ahead</li>
			<li><strong>Judges & Tournament Organizers</strong> - To verify correct token counts in competitive play</li>
		</ul>
	</section>

	<section>
		<h2>Open Source</h2>
		<p>
			The Scute Swarm Calculator is free to use and open source. We believe in providing useful tools to the 
			Magic: The Gathering community without barriers.
		</p>
		<p>
			If you have suggestions for improvements or find any bugs, feel free to reach out or contribute to the project.
		</p>
	</section>
</article>

<style>
	article {
		max-width: 800px;
		margin: 0 auto;
		padding: 2rem 1rem;
		line-height: 1.7;
	}

	h1 {
		color: #2e7d32;
		margin-bottom: 1.5rem;
		text-align: center;
	}

	h2 {
		color: #388e3c;
		margin-top: 2rem;
		margin-bottom: 1rem;
		border-bottom: 2px solid #81c784;
		padding-bottom: 0.5rem;
	}

	section {
		margin-bottom: 2rem;
	}

	p {
		margin-bottom: 1rem;
		text-align: justify;
	}

	blockquote {
		background: #f1f8e9;
		border-left: 4px solid #4caf50;
		padding: 1rem 1.5rem;
		margin: 1.5rem 0;
		font-style: italic;
		border-radius: 0 8px 8px 0;
	}

	ul {
		margin: 1rem 0;
		padding-left: 2rem;
	}

	li {
		margin-bottom: 0.5rem;
	}

	a {
		color: #1976d2;
		text-decoration: none;
	}

	a:hover {
		text-decoration: underline;
	}
</style>
