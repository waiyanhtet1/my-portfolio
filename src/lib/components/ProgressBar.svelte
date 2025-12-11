<script lang="ts">
	import { onMount } from 'svelte';
	import Button from './Button.svelte';

	let progress = 0;
	let loadingText = '';

	onMount(() => {
		const interval = setInterval(() => {
			if (progress >= 100) {
				loadingText = 'Done!';
				clearInterval(interval);
			} else {
				progress += 1;
				loadingText = `Initializing System... ${progress}%`;
			}
		}, 10);
	});
</script>

{#if progress >= 100}
	<a href="/home">
		<Button>enter the system</Button>
	</a>
{:else}
	<div class="progress-container">
		<div class="progress-bar" style="width: {progress}%"></div>
		<div class="progress-text">{loadingText}</div>
	</div>
{/if}

<style>
	.progress-container {
		position: relative;
		width: 100%;
		height: 20px;
		background-color: transparent;
		overflow: hidden;
		margin: 20px 0;
	}

	.progress-bar {
		height: 100%;
		background-color: var(--primary);
		width: 0%;
		transition: width 0.2s ease;
	}

	.progress-text {
		position: absolute;
		width: 100%;
		text-align: center;
		top: 0;
		left: 0;
		line-height: 20px;
		font-weight: bold;
		color: white;
		text-shadow: 0 0 2px black;
	}
</style>
