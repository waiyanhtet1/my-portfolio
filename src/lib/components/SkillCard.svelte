<script lang="ts">
	import type { ColorType } from '$lib/types/SkillType';
	import { onMount } from 'svelte';

	interface Props {
		color: ColorType;
		name: string;
		icon: string;
	}

	let { color, name, icon }: Props = $props();
	let clickSound: HTMLAudioElement;

	onMount(() => {
		clickSound = new Audio('/assets/sounds/hover.wav');
	});

	function playSound() {
		if (clickSound) {
			clickSound.currentTime = 0;
			clickSound.play();
		}
	}
</script>

<button class="container {color}" onmouseenter={playSound}>
	<img src={icon} alt="" />

	<p class={color}>{name}</p>
</button>

<style>
	.container {
		min-width: 100px;
		border-top: 1px solid var(--border-gray-dark);
		border-left: 1px solid var(--border-gray-dark);
		border-right: 1px solid var(--border-gray-dark);
		display: flex;
		flex-direction: column;
		align-items: center;
		cursor: pointer;
		background-color: transparent;
	}

	.container:hover {
		transform: scale(1.1);
	}

	img {
		padding: 10px;
		width: 100%;
		height: 70px;
		object-fit: contain;
	}

	p {
		width: 100%;
		padding: 5px 10px;
		text-align: center;
		font-family: var(--secondary-font);
		font-size: 18px;
		background-color: var(--primary);
		text-transform: uppercase;
	}

	p.red {
		background-color: var(--primary);
	}

	p.green {
		background-color: var(--green);
	}

	p.blue {
		background-color: var(--blue);
	}

	p.yellow {
		background-color: var(--yellow);
	}
</style>
