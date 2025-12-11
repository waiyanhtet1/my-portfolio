<script lang="ts">
	import LeftSideBar from '$lib/sections/LeftSideBar.svelte';
	import Navbar from '$lib/sections/Navbar.svelte';
	import RightSideBar from '$lib/sections/RightSideBar.svelte';
</script>

<div class="whole-container">
	<Navbar />

	<div class="container">
		<LeftSideBar />
		<slot />
		<RightSideBar />
	</div>
</div>

<style>
	.whole-container {
		margin: 10px 2rem;
	}

	.container {
		display: flex;
		justify-content: space-between;
		margin-top: 1.5rem;
	}
</style>
