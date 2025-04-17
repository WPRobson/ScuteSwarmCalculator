<script lang="ts">
	import { spring } from 'svelte/motion';

	interface Props {
		count?: number;
	}

	let { count = $bindable(0) }: Props = $props();

	const displayed_count = spring();
	let view = $derived(count);
	//$: offset = modulo($displayed_count, 1);

	// function modulo(n: number, m: number) {
	// 	// handle negative numbers
	// 	return ((n % m) + m) % m;
	// }
</script>

<div class="counter">
	<button onclick={() => (count -= 1)} aria-label="Decrease the counter by one">
		<svg aria-hidden="true" viewBox="0 0 1 1">
			<path d="M0,0.5 L1,0.5" />
		</svg>
	</button>

	<div class="counter-viewport">
		<div class="counter-digits">
			<!-- <strong class="hidden" aria-hidden="true">{Math.floor($displayed_count + 1)}</strong> -->
			<!-- <strong>{$view}</strong> -->
			<strong>{view}</strong>
		</div>
	</div>

	<button onclick={() => (count += 1)} aria-label="Increase the counter by one">
		<svg aria-hidden="true" viewBox="0 0 1 1">
			<path d="M0,0.5 L1,0.5 M0.5,0 L0.5,1" />
		</svg>
	</button>
</div>

<style>
	.counter {
		display: flex;
		width: fit-content;
		border-top: 1px solid rgba(0, 0, 0, 0.1);
		border-bottom: 1px solid rgba(0, 0, 0, 0.1);
		/* margin: 0.3rem 0; */
	}

	.counter button {
		width: 2em;
		padding: 0;
		display: flex;
		align-items: center;
		justify-content: center;
		border: 0;
		background-color: transparent;
		touch-action: manipulation;
		font-size: 2rem;
	}

	.counter button:hover {
		background-color: var(--color-bg-1);
	}

	svg {
		width: 25%;
		height: 25%;
	}

	path {
		vector-effect: non-scaling-stroke;
		stroke-width: 2px;
		stroke: #444;
	}

	.counter-viewport {
		width: 8em;
		height: 4em;
		/* overflow: hidden; */
		text-align: center;
		position: relative;
	}

	.counter-viewport strong {
		position: absolute;
		display: flex;
		width: 100%;
		height: 100%;
		font-weight: 400;
		color: var(--color-theme-1);
		font-size: 4rem;
		align-items: center;
		justify-content: center;
	}

	.counter-digits {
		position: absolute;
		width: 100%;
		height: 100%;
	}

	/* .hidden {
		top: -100%;
		user-select: none;
	} */
</style>
