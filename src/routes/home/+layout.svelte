<script lang="ts">
	import LeftSideBar from '$lib/sections/LeftSideBar.svelte';
	import Navbar from '$lib/sections/Navbar.svelte';
</script>

<div class="whole-container">
	<Navbar />

	<div class="container">
		<LeftSideBar />
		<slot />
	</div>
</div>

<style>
	.whole-container {
		margin: 10px 2rem;
	}

	.container {
		display: flex;
		margin-top: 1rem;
	}
</style>
