<script>
	import Button from '$lib/components/Button.svelte';
</script>

<div class="container">
	<h1>Hi!</h1>

	<div class="sub-title-container">
		<p class="sub-title">Welcome to by personal website.</p>
		<p class="sub-title-description1">
			I have created this website to feel like a game/sci-fi interface. All text inside tries to
			reflect this.
		</p>
		<p class="sub-title-description2">
			You will find fully information of my professional life and are related to what I am working
			on.
		</p>
		<Button onClick={() => alert('button was clicked')}>enter the system</Button>
	</div>
</div>

<!-- <Canvas>
	<T.Color attach="background" args={['#000003']} />

	<Scene />
</Canvas> -->

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
