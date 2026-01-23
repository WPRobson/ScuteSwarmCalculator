<script>
	export const prerender = true;
	import Header from './Header.svelte';
	import './styles.css';
	import { base } from '$app/paths';
	/** @type {{children?: import('svelte').Snippet}} */
	let { children } = $props();
</script>

<div class="app">
	<Header />

	<main>
		{@render children?.()}
	</main>

	<footer>
		<div class="footer-content">
			<div class="footer-links">
				<a href="{base}/">Calculator</a>
				<a href="{base}/guide">Strategy Guide</a>
				<a href="{base}/about">About</a>
			</div>
			<p class="disclaimer">
				Scute Swarm Calculator is an unofficial fan tool. Magic: The Gathering is a trademark of Wizards of the Coast LLC.
			</p>
			<p class="copyright">© 2026 Scute Swarm Calculator. All rights reserved.</p>
		</div>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		/* padding: 1rem; */
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 2rem 1rem;
		background: #f5f5f5;
		border-top: 1px solid #e0e0e0;
		margin-top: 2rem;
	}

	.footer-content {
		max-width: 800px;
		text-align: center;
	}

	.footer-links {
		display: flex;
		gap: 1.5rem;
		justify-content: center;
		flex-wrap: wrap;
		margin-bottom: 1rem;
	}

	.footer-links a {
		color: #555;
		text-decoration: none;
		font-size: 0.9rem;
	}

	.footer-links a:hover {
		color: #2e7d32;
		text-decoration: underline;
	}

	.disclaimer {
		font-size: 0.8rem;
		color: #777;
		margin-bottom: 0.5rem;
	}

	.copyright {
		font-size: 0.8rem;
		color: #999;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
