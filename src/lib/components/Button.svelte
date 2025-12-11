<script lang="ts">
	import { onMount, type Snippet } from 'svelte';

	interface Props {
		children: Snippet;
		onClick?: () => void;
	}

	let { children, onClick }: Props = $props();

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

<button onclick={playSound}>
	{@render children()}
</button>

<style>
	button {
		background-color: transparent;
		border: 1px solid var(--primary);
		padding: 10px 30px;
		text-transform: uppercase;
		color: var(--primary);
		font-family: var(--primary-font);
		font-size: 18px;
		font-weight: bold;
		cursor: pointer;
	}

	button:hover {
		box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
		-webkit-box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
		-moz-box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
	}
</style>
