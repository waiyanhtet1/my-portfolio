<script lang="ts">
	import { onMount } from 'svelte';

	let time = '';

	function formatTime(date: Date) {
		let hours = date.getHours();
		const minutes = date.getMinutes();
		const seconds = date.getSeconds();

		const ampm = hours >= 12 ? 'PM' : 'AM';
		hours = hours % 12 || 12;

		const pad = (num: number) => String(num).padStart(2, '0');

		return `${pad(hours)}:${pad(minutes)}:${pad(seconds)} ${ampm}`;
	}

	onMount(() => {
		setInterval(() => {
			setTimeout(() => {
				time = formatTime(new Date());
			}, 150);
		}, 1000);
	});
</script>

<div class="clock">
	<span>{time}</span>
</div>

<style>
	.clock {
		color: var(--gray);
		font-family: var(--secondary-font);
		font-size: 18px;
	}

	span {
		display: inline-block;
		transition:
			opacity 0.15s ease,
			transform 0.15s ease;
	}
</style>
