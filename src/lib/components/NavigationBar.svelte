<script lang="ts">
	import { page } from '$app/state';
	import { Box, BrainCircuit, CalendarFold, FolderCode, Headset } from '@lucide/svelte';
	import { onMount } from 'svelte';

	let currentPath = $derived(page.url.pathname);
	let clickSound: HTMLAudioElement;

	onMount(() => {
		clickSound = new Audio('/assets/sounds/click.wav');
	});

	function playSound() {
		if (clickSound) {
			clickSound.currentTime = 0;
			clickSound.play();
		}
	}
</script>

<div class="nav-bar">
	<div class="container">
		<a href="/home" class="nav-item {currentPath === '/home' && 'active'}" onclick={playSound}>
			<div class="nav-header {currentPath === '/home' && 'active'}">
				<p>ProtoNex-V</p>
				<BrainCircuit color={'black'} />
			</div>
			<p class="nav-desc">3D rendering robot</p>
		</a>

		<a
			href="/home/skills"
			class="nav-item {currentPath === '/home/skills' && 'active'}"
			onclick={playSound}
		>
			<div class="nav-header {currentPath === '/home/skills' && 'active'}">
				<p>Skills</p>
				<Box color={'black'} />
			</div>
			<p class="nav-desc">My career working skills</p>
		</a>

		<div class="nav-item">
			<div class="nav-header">
				<p>Projects</p>
				<FolderCode color={'black'} />
			</div>
			<p class="nav-desc">Production Projects</p>
		</div>

		<div class="nav-item">
			<div class="nav-header">
				<p>Timeline</p>
				<CalendarFold color={'black'} />
			</div>
			<p class="nav-desc">Working Histories</p>
		</div>

		<div class="nav-item">
			<div class="nav-header">
				<p>Contact</p>
				<Headset color={'black'} />
			</div>
			<p class="nav-desc">Reach to me</p>
		</div>
	</div>
</div>

<style>
	.nav-bar {
		/* position: relative; */
	}

	.container {
		position: absolute;
		bottom: -25px;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 1rem;
		width: 100%;
	}

	.nav-item {
		border-left: 3px solid var(--bg-gray);
		width: 170px;
		cursor: pointer;
		transition: border-color 0.3s ease;
	}

	.nav-item.active {
		border-left: 3px solid var(--primary);
	}

	.nav-header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 1rem;
		font-weight: bold;
		background-color: var(--bg-gray);
		letter-spacing: 1px;
		font-size: 18px;
		text-transform: uppercase;
		padding: 5px 10px;
		color: white;
		transition: border-color 0.3s ease;
	}

	.nav-header.active {
		background-color: var(--primary);
	}

	.nav-desc {
		font-size: 14px;
		color: var(--gray);
		padding: 5px;
		font-family: var(--secondary-font);
	}

	.nav-item:hover {
		box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
		-webkit-box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
		-moz-box-shadow: 0px 0px 150px 16px rgba(232, 74, 74, 0.75);
	}
</style>
