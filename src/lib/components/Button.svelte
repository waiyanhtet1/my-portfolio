<script lang="ts">
	import { onMount, type Snippet } from 'svelte';

	interface Props {
		size?: 'md' | 'sm';
		children: Snippet;
		onClick?: () => void;
	}

	let { size = 'md', children, onClick }: Props = $props();
	let clickSound: HTMLAudioElement;

	onMount(() => {
		clickSound = new Audio('/assets/sounds/click.wav');
	});

	function playSound() {
		if (clickSound) {
			clickSound.currentTime = 0;
			clickSound.play();
		}

		if (onClick) onClick();
	}
</script>

<button onclick={playSound} class={size === 'md' ? 'md' : 'sm'}>
	{@render children()}
</button>

<style>
	button {
		display: flex;
		align-items: center;
		justify-content: space-between;
		background-color: transparent;
		border: 1px solid var(--primary);
		text-transform: uppercase;
		color: var(--primary);
		font-family: var(--primary-font);
		font-weight: bold;
		cursor: pointer;
	}

	button:hover {
		box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
		-webkit-box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
		-moz-box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
	}

	.md {
		padding: 10px 30px;
		font-size: 18px;
	}
	.sm {
		padding: 5px 10px;
		font-size: 16px;
	}
</style>
