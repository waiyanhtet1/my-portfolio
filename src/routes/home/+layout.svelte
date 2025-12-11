<script lang="ts">
	import NavigationBar from '$lib/components/NavigationBar.svelte';
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

	<NavigationBar />
</div>

<style>
	.whole-container {
		margin: 10px 1rem;
		position: relative;
	}

	.container {
		display: flex;
		justify-content: space-between;
		margin-top: 1rem;
	}
</style>
