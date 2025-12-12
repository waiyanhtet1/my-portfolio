<script lang="ts">
	import SkillCard from '$lib/components/SkillCard.svelte';
	import { skills } from '$lib/constants/skill';
</script>

<div class="container">
	<span class="top-right"></span>
	<span class="bottom-left"></span>

	<h3>skills</h3>

	<div class="header-top"></div>

	<div class="skills">
		{#each skills as skill}
			<SkillCard color={skill.color} name={skill.name} icon={skill.icon} />
		{/each}
	</div>
</div>

<style>
	.container {
		width: 100%;
		height: 600px;
		position: relative;
		border: 1px solid var(--border-gray);
		margin: 0 10px;
		padding: 15px 20px;
	}

	.container::before,
	.container::after {
		content: '';
		position: absolute;
		width: 7px;
		height: 7px;
		border: 3px solid #ff2a2a;
	}

	.container::before {
		top: -2px;
		left: -2px;
		border-right: none;
		border-bottom: none;
	}

	.container::after {
		bottom: -3px;
		right: -2px;
		border-left: none;
		border-top: none;
	}

	.container span {
		position: absolute;
		width: 7px;
		height: 7px;
		border: 3px solid #ff2a2a;
	}

	.container span.top-right {
		top: -2px;
		right: -2px;
		border-left: none;
		border-bottom: none;
	}

	.container span.bottom-left {
		bottom: -3px;
		left: -2px;
		border-right: none;
		border-top: none;
	}

	h3 {
		color: white;
		font-family: var(--secondary-font);
		letter-spacing: 2px;
		text-transform: uppercase;
		text-align: center;
	}

	.header-top {
		margin: 10px 0;
		border-top: 3px solid var(--primary);
		height: 20px;
		background-color: var(--secondary);
	}

	.skills {
		display: flex;
		align-items: center;
		gap: 1rem;
		flex-wrap: wrap;
	}
</style>
