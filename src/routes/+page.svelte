<script>
	import ProgressBar from '$lib/components/ProgressBar.svelte';
	import { fade, fly } from 'svelte/transition';
</script>

<div class="container">
	<h1 in:fade out:fade>Hi!</h1>

	<div class="sub-title-container" in:fly={{ x: 50 }} out:fly={{ x: 50 }}>
		<p class="sub-title">Welcome to by personal website.</p>
		<p class="sub-title-description1">
			I have created this website to feel like a game/sci-fi interface. All text inside tries to
			reflect this.
		</p>
		<p class="sub-title-description2">
			You will find fully information of my professional life and are related to what I am working
			on.
		</p>
		<p class="sub-title-description2">
			!! Be aware when you enter the system the sound will start !!
		</p>

		<ProgressBar />
	</div>
</div>

<style>
	.container {
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 5rem;
		width: 1000px;
		height: 90vh;
		margin: 0 auto;
	}
	h1 {
		color: var(--primary);
		font-size: 20rem;
	}

	.sub-title-container {
		color: white;
		font-family: var(--secondary-font);
	}

	.sub-title {
		font-size: 22px;
	}

	.sub-title-description1,
	.sub-title-description2 {
		font-size: 18px;
	}
</style>
