<script lang="ts">
	import reward1 from '$lib/assets/reward-1.png';
	import reward2 from '$lib/assets/reward-2.png';
	import { BrainCircuit } from '@lucide/svelte';
</script>

<div class="container">
	<div>
		<div class="quest-header">
			<p>Specification</p>
			<BrainCircuit />
		</div>

		<p class="quest-item">Mobile Application Development</p>
		<p class="quest-item">Website Application Development</p>
	</div>

	<div class="quest">
		<p class="key">developed portfolio by</p>
		<p class="value">SvelteKit</p>
		<p class="value">Javascript</p>
		<p class="value">Svelte Threlte</p>
		<p class="value">3D model</p>
	</div>

	<div class="rewards">
		<p>Rewards</p>

		<div class="imgs">
			<div class="img">
				<img src={reward1} alt="" />
				<p>+5</p>
			</div>
			<div class="img">
				<img src={reward2} alt="" />
				<p>+25</p>
			</div>
		</div>
	</div>
</div>

<style>
	.container {
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
	}

	.quest-header {
		background-color: var(--primary);
		padding: 5px 10px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		color: var(--primary-bg);
		text-transform: uppercase;
		/* font-size: 20px; */
		letter-spacing: 1px;
		font-weight: bold;
	}

	.quest-item {
		background-color: var(--secondary);
		color: var(--gray);
		font-family: var(--secondary-font);
		font-size: 18px;
		padding: 3px 10px;
	}

	.quest {
		text-transform: uppercase;
		letter-spacing: 2px;
	}

	.quest .key {
		color: white;
		font-family: var(--secondary-font);
		margin-bottom: 5px;
	}

	.quest .value {
		color: var(--primary);
		font-weight: bold;
	}

	.rewards {
		color: white;
		font-family: var(--secondary-font);
		text-transform: uppercase;
		font-size: 18px;
		letter-spacing: 2px;
	}

	.rewards p {
		margin-bottom: 5px;
	}

	.imgs {
		display: flex;
		align-items: center;
		gap: 10px;
	}
	.imgs .img {
		display: flex;
		flex-direction: column;
		align-items: center;
		color: var(--gray);
	}
</style>
