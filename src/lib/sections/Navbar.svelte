<script lang="ts">
	import AnimatedClock from '$lib/components/AnimatedClock.svelte';
</script>

<nav>
	<div class="level">
		<p>25</p>
		<p>level</p>
	</div>
	<div class="times">
		<p>Local time:</p>
		<AnimatedClock />
	</div>
</nav>

<style>
	nav {
		display: flex;
		align-items: center;
		justify-content: space-between;
		text-transform: uppercase;
	}

	.level {
		display: flex;
		align-items: flex-end;
		gap: 5px;
		font-weight: bold;
	}

	.level p:first-child {
		font-size: 25px;
		color: var(--green);
	}

	.level p:last-child {
		font-size: 18px;
		color: var(--gray);
	}

	.times {
		display: flex;
		align-items: center;
		align-self: flex-end;
		gap: 3px;
		font-family: var(--secondary-font);
		font-size: 18px;
	}

	.times p:first-child {
		color: var(--gray);
	}

	.times p:last-child {
		color: white;
	}
</style>
