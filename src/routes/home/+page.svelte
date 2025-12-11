<script>
	import QuoteTyper from '$lib/components/QuoteTyper.svelte';
	import Scene from '$lib/components/Scene.svelte';
	import { Canvas } from '@threlte/core';
</script>

<div class="container">
	<Canvas>
		<!-- <T.Color attach="background" args={['#000003']} /> -->
		<Scene />
	</Canvas>

	<span class="top-right"></span>
	<span class="bottom-left"></span>

	<h1>ProtoNex-V</h1>

	<div class="spec">
		<p>Height: 1.35 m</p>
		<p>Weight: 42 kg</p>
		<p>Frame Material: Lightweight titanium-polymer hybrid</p>
		<p>Omni-wheel rotational base</p>
		<p>Stabilized gyroscopic balancing</p>
		<p>Capable of smooth terrain traversal indoors and outdoors</p>
	</div>

	<div class="power">
		<p>CoreCell V-Fusion Battery</p>
		<p>18 hours continuous operation</p>
		<p>Auto-dock recharge system</p>
		<p>Low-power adaptive standby mode</p>
	</div>

	<div class="interation">
		<p>Voice Interface: V-Synth 2.0 (clear, customizable voice output)</p>
		<p>Data Collector Mode</p>
		<p>Navigation & Mapping Mode</p>
		<p>Assistance Mode (non-hazard tasks only)</p>
		<p>Display: 7-inch holographic mini-panel for visual output</p>
	</div>

	<QuoteTyper />
</div>

<style>
	.container {
		width: 100vw;
		height: 600px;
		position: relative;
		border: 1px solid var(--border-gray);
		margin: 0 10px;
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

	h1 {
		position: absolute;
		bottom: 50px;
		right: 5px;
		color: var(--primary);
		font-family: var(--secondary-font);
	}
	.spec {
		position: absolute;
		right: 10px;
		bottom: 85px;
		color: var(--gray);
		text-align: right;
		font-family: var(--secondary-font);
	}

	.power {
		position: absolute;
		top: 10px;
		right: 10px;
		color: var(--gray);
		text-align: right;
		font-family: var(--secondary-font);
	}

	.interation {
		position: absolute;
		left: 10px;
		bottom: 60px;
		color: var(--gray);
		font-family: var(--secondary-font);
	}
</style>
