<script>
	import { BrainCircuit } from '@lucide/svelte';
</script>

<div class="nav-bar">
	<div class="container">
		<div class="nav-item">
			<div class="nav-header">
				<p>ProtoNex-V</p>
				<BrainCircuit color={'black'} />
			</div>
			<p class="nav-desc">3D rendering robot</p>
		</div>

		<div class="nav-item">
			<div class="nav-header">
				<p>Skills</p>
				<BrainCircuit color={'black'} />
			</div>
			<p class="nav-desc">My career working skills</p>
		</div>

		<div class="nav-item">
			<div class="nav-header">
				<p>Projects</p>
				<BrainCircuit color={'black'} />
			</div>
			<p class="nav-desc">Production Projects</p>
		</div>

		<div class="nav-item">
			<div class="nav-header">
				<p>Timeline</p>
				<BrainCircuit color={'black'} />
			</div>
			<p class="nav-desc">Working Histories</p>
		</div>

		<div class="nav-item">
			<div class="nav-header">
				<p>Contact</p>
				<BrainCircuit color={'black'} />
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
		border-left: 3px solid var(--primary);
		width: 170px;
		cursor: pointer;
	}

	.nav-header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 1rem;
		font-weight: bold;
		background-color: var(--primary);
		letter-spacing: 1px;
		font-size: 18px;
		text-transform: uppercase;
		padding: 5px 10px;
		color: white;
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
