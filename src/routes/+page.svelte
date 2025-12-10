<script>
	import Scene from '$lib/components/Scene.svelte';
	import { Canvas, T } from '@threlte/core';
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<Canvas>
	<T.Color attach="background" args={['#000003']} />

	<Scene />
</Canvas>
