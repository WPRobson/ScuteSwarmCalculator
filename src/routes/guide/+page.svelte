<script>
	import { base } from '$app/paths';
</script>

<svelte:head>
	<title>Scute Swarm Strategy Guide - Tips & Combos for MTG</title>
	<meta name="description" content="Master Scute Swarm with our comprehensive strategy guide. Learn the best combos, deck building tips, and how to maximize your landfall triggers in Magic: The Gathering." />
	<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-4072443652630199" crossorigin="anonymous"></script>
</svelte:head>

<article>
	<h1>Scute Swarm Strategy Guide</h1>
	<p class="intro">
		Master the art of exponential token generation with our comprehensive guide to playing Scute Swarm 
		in Magic: The Gathering.
	</p>

	<nav class="toc">
		<h2>Table of Contents</h2>
		<ol>
			<li><a href="#card-analysis">Card Analysis</a></li>
			<li><a href="#key-combos">Key Combos & Synergies</a></li>
			<li><a href="#deck-building">Deck Building Tips</a></li>
			<li><a href="#play-patterns">Play Patterns</a></li>
			<li><a href="#counters">How to Counter Scute Swarm</a></li>
			<li><a href="#formats">Format Considerations</a></li>
		</ol>
	</nav>

	<section id="card-analysis">
		<h2>Card Analysis</h2>
		<div class="card-details">
			<h3>Scute Swarm</h3>
			<p><strong>Mana Cost:</strong> 2G (3 mana total)</p>
			<p><strong>Type:</strong> Creature — Insect</p>
			<p><strong>Power/Toughness:</strong> 1/1</p>
			<p><strong>Set:</strong> Zendikar Rising (ZNR)</p>
		</div>
		
		<h3>Strengths</h3>
		<ul>
			<li><strong>Low mana cost</strong> - At just 3 mana, Scute Swarm can come down early and start generating value</li>
			<li><strong>Exponential scaling</strong> - Once you hit 6 lands, your board presence multiplies rapidly</li>
			<li><strong>Resilient strategy</strong> - Even one surviving Scute can rebuild your army</li>
			<li><strong>Green color identity</strong> - Access to the best land ramp in the game</li>
		</ul>

		<h3>Weaknesses</h3>
		<ul>
			<li><strong>Slow start</strong> - Needs time to set up before becoming threatening</li>
			<li><strong>Vulnerable to board wipes</strong> - A single Wrath effect resets everything</li>
			<li><strong>No evasion</strong> - Tokens can be blocked by anything</li>
			<li><strong>Depends on lands</strong> - Land destruction disrupts the strategy</li>
		</ul>
	</section>

	<section id="key-combos">
		<h2>Key Combos & Synergies</h2>
		
		<h3>Ramp Spells That Put Multiple Lands Into Play</h3>
		<p>These cards trigger Scute Swarm multiple times at once:</p>
		<ul>
			<li><strong><a href="https://scryfall.com/card/fdn/635/circuitous-route" target="_blank" rel="noopener">Circuitous Route</a></strong> - 2 lands at once</li>
			<li><strong><a href="https://scryfall.com/card/ecc/113/kodamas-reach" target="_blank" rel="noopener">Kodama's Reach</a></strong> - 1 to battlefield, 1 to hand</li>
			<li><strong><a href="https://scryfall.com/card/soc/265/cultivate" target="_blank" rel="noopener">Cultivate</a></strong> - Same as Kodama's Reach</li>
			<li><strong><a href="https://scryfall.com/card/m13/162/boundless-realms" target="_blank" rel="noopener">Boundless Realms</a></strong> - Doubles your basics (game-ending with Scute)</li>
			<li><strong><a href="https://scryfall.com/card/znr/185/ashaya-soul-of-the-wild" target="_blank" rel="noopener">Ashaya, Soul of the Wild</a></strong> - Makes all your creatures into lands too!</li>
		</ul>

		<h3>Protection and Recursion</h3>
		<ul>
			<li><strong><a href="https://scryfall.com/card/cmm/295/heroic-intervention" target="_blank" rel="noopener">Heroic Intervention</a></strong> - Protects from board wipes</li>
			<li><strong><a href="https://scryfall.com/card/cmm/286/eternal-witness" target="_blank" rel="noopener">Eternal Witness</a></strong> - Get back destroyed Scutes</li>
			<li><strong><a href="https://scryfall.com/card/mh1/166/genesis" target="_blank" rel="noopener">Genesis</a></strong> - Recurring creature retrieval</li>
		</ul>

		<h3>Payoffs for Having Many Creatures</h3>
		<ul>
			<li><strong><a href="https://scryfall.com/card/dsc/192/overwhelming-stampede" target="_blank" rel="noopener">Overwhelming Stampede</a></strong> - Turn tokens into a lethal force</li>
			<li><strong><a href="https://scryfall.com/card/ncc/283/beastmaster-ascension" target="_blank" rel="noopener">Beastmaster Ascension</a></strong> - +5/+5 to all creatures</li>
			<li><strong><a href="https://scryfall.com/card/tdm/138/craterhoof-behemoth" target="_blank" rel="noopener">Craterhoof Behemoth</a></strong> - The classic finisher</li>
			<li><strong><a href="https://scryfall.com/card/mom/211/tribute-to-the-world-tree" target="_blank" rel="noopener">Tribute to the World Tree</a></strong> - Mana fixing with creature lands</li>
		</ul>

		<h3>The Ashaya Combo</h3>
		<p>
			One of the most powerful interactions is with <strong>Ashaya, Soul of the Wild</strong>. When Ashaya is on the 
			battlefield, all your nontoken creatures become Forest lands in addition to their other types. This means:
		</p>
		<ol>
			<li>Your Scute Swarm tokens enter as lands</li>
			<li>Each token entering triggers all other Scute Swarms</li>
			<li>This creates an infinite loop (usually stopped by the game rules at a very large number)</li>
		</ol>
		<p class="warning">
			⚠️ In paper Magic, you'll need to agree on a number with your opponent. Our calculator can help you 
			determine exact counts for specific scenarios.
		</p>
	</section>

	<section id="deck-building">
		<h2>Deck Building Tips</h2>
		
		<h3>Mana Base</h3>
		<p>
			Since Scute Swarm cares about lands entering, your mana base is crucial:
		</p>
		<ul>
			<li>Run 36-40 lands in Commander (higher than average)</li>
			<li>Include fetch lands to trigger landfall multiple times per turn</li>
			<li>Consider land recursion like <a href="https://scryfall.com/card/otc/202/ramunap-excavator" target="_blank" rel="noopener">Ramunap Excavator</a></li>
			<li>Use MDFCs (Modal Double-Faced Cards) that are lands on one side</li>
		</ul>

		<h3>Supporting Cards</h3>
		<p>Build your deck around these categories:</p>
		<ul>
			<li><strong>Ramp (15-20 cards)</strong> - Focus on cards that put lands onto the battlefield</li>
			<li><strong>Card Draw (8-10 cards)</strong> - Keep the lands flowing</li>
			<li><strong>Protection (5-8 cards)</strong> - Protect your Scutes from removal</li>
			<li><strong>Finishers (3-5 cards)</strong> - Win after you've built your army</li>
		</ul>

		<h3>Sample Commander Pairings</h3>
		<ul>
			<li><strong><a href="https://scryfall.com/card/znr/232/omnath-locus-of-creation" target="_blank" rel="noopener">Omnath, Locus of Creation</a></strong> - 4-color landfall powerhouse</li>
			<li><strong><a href="https://scryfall.com/card/cmr/239/kodama-of-the-east-tree" target="_blank" rel="noopener">Kodama of the East Tree</a></strong> - Put additional permanents into play</li>
			<li><strong><a href="https://scryfall.com/card/znr/234/phylath-world-sculptor" target="_blank" rel="noopener">Phylath, World Sculptor</a></strong> - More token synergy</li>
			<li><strong><a href="https://scryfall.com/card/ecc/129/omnath-locus-of-rage" target="_blank" rel="noopener">Omnath, Locus of Rage</a></strong> - Elemental token synergy</li>
		</ul>
	</section>

	<section id="play-patterns">
		<h2>Play Patterns</h2>
		
		<h3>Early Game (Turns 1-4)</h3>
		<ol>
			<li>Play ramp spells to accelerate your land count</li>
			<li>Deploy Scute Swarm when you have 4-5 lands</li>
			<li>Don't rush it out on turn 3 if it will just be removed</li>
		</ol>

		<h3>Mid Game (Turns 5-7)</h3>
		<ol>
			<li>Hit 6 lands and start exponential growth</li>
			<li>Play multiple lands per turn if possible</li>
			<li>Hold protection spells for board wipes</li>
		</ol>

		<h3>Late Game (Turn 8+)</h3>
		<ol>
			<li>Your board should be overwhelming by now</li>
			<li>Use finishers to push through damage</li>
			<li>Consider leaving some Scutes back as blockers</li>
		</ol>

		<h3>Combat Math Tips</h3>
		<p>
			With large numbers of tokens, combat can get complicated. Use our calculator to track:
		</p>
		<ul>
			<li>Exact token counts after each landfall trigger</li>
			<li>Total damage output with pump effects</li>
			<li>How many tokens you need to hold back for defense</li>
		</ul>
	</section>

	<section id="counters">
		<h2>How to Counter Scute Swarm</h2>
		<p>If you're facing a Scute Swarm deck, here's how to fight back:</p>
		
		<h3>Removal Timing</h3>
		<ul>
			<li>Kill Scute Swarm before they hit 6 lands</li>
			<li>Board wipes are most effective, not spot removal</li>
			<li>Use instant-speed removal during landfall triggers</li>
		</ul>

		<h3>Effective Counter Cards</h3>
		<ul>
			<li><strong><a href="https://scryfall.com/card/fdn/754/massacre-wurm" target="_blank" rel="noopener">Massacre Wurm</a></strong> - Kills tokens and drains life</li>
			<li><strong><a href="https://scryfall.com/card/dtk/125/virulent-plague" target="_blank" rel="noopener">Virulent Plague</a></strong> - Kills all 1/1 tokens on entry</li>
			<li><strong><a href="https://scryfall.com/card/eoc/125/rakdos-charm" target="_blank" rel="noopener">Rakdos Charm</a></strong> - Deals damage equal to creatures controlled</li>
			<li><strong><a href="https://scryfall.com/card/khm/9/doomskar" target="_blank" rel="noopener">Doomskar</a></strong> - Board wipe that can be foretold</li>
		</ul>
	</section>

	<section id="formats">
		<h2>Format Considerations</h2>
		
		<h3>Commander/EDH</h3>
		<p>
			Scute Swarm shines brightest in Commander. The longer games and higher land counts make exponential growth 
			almost inevitable. It's a staple in landfall-themed decks.
		</p>

		<h3>Standard (When Legal)</h3>
		<p>
			In Standard, Scute Swarm saw competitive play in various Gruul and Simic landfall decks. The faster format 
			means you have less time to set up, but the payoff is still game-winning.
		</p>

		<h3>Pioneer & Modern</h3>
		<p>
			While not a format staple, Scute Swarm can be a budget-friendly win condition in ramp strategies. The faster 
			nature of these formats makes it more of a casual choice.
		</p>
	</section>

	<section class="cta">
		<h2>Ready to Calculate?</h2>
		<p>
			Now that you understand Scute Swarm strategy, use our <a href="{base}/">Scute Swarm Calculator</a> to track your 
			tokens during your next game!
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

	.intro {
		font-size: 1.2rem;
		color: #555;
		text-align: center;
		margin-bottom: 2rem;
		font-style: italic;
	}

	.toc {
		background: #f5f5f5;
		padding: 1.5rem 2rem;
		border-radius: 8px;
		margin-bottom: 2rem;
	}

	.toc h2 {
		margin-top: 0;
		font-size: 1.2rem;
	}

	.toc ol {
		margin: 0;
		padding-left: 1.5rem;
	}

	.toc li {
		margin-bottom: 0.3rem;
	}

	.toc a {
		color: #1976d2;
		text-decoration: none;
	}

	.toc a:hover {
		text-decoration: underline;
	}

	h1 {
		color: #2e7d32;
		margin-bottom: 1rem;
		text-align: center;
	}

	h2 {
		color: #388e3c;
		margin-top: 2.5rem;
		margin-bottom: 1rem;
		border-bottom: 2px solid #81c784;
		padding-bottom: 0.5rem;
	}

	h3 {
		color: #43a047;
		margin-top: 1.5rem;
		margin-bottom: 0.75rem;
	}

	.card-details {
		background: #e8f5e9;
		padding: 1rem 1.5rem;
		border-radius: 8px;
		margin-bottom: 1.5rem;
	}

	.card-details h3 {
		margin-top: 0;
		color: #2e7d32;
	}

	.card-details p {
		margin: 0.3rem 0;
	}

	section {
		margin-bottom: 2rem;
	}

	p {
		margin-bottom: 1rem;
	}

	ul, ol {
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

	.warning {
		background: #fff3e0;
		border-left: 4px solid #ff9800;
		padding: 1rem 1.5rem;
		margin: 1.5rem 0;
		border-radius: 0 8px 8px 0;
	}

	.cta {
		background: #e8f5e9;
		padding: 2rem;
		border-radius: 8px;
		text-align: center;
		margin-top: 3rem;
	}

	.cta h2 {
		border: none;
		margin-top: 0;
	}

	.cta a {
		color: #2e7d32;
		font-weight: bold;
	}
</style>
