<script lang="ts">
	import { T } from '@threlte/core';
	import { OrbitControls, useDraco, useGltf, useGltfAnimations } from '@threlte/extras';

	const dracoLoader = useDraco();
	const gltf = useGltf('/assets/robot.glb', { dracoLoader });
	const { actions } = useGltfAnimations<'Orange_black_sci_fi_unit2|A|2025_11_6_15_24_13'>(gltf);

	$effect(() => {
		$actions['Orange_black_sci_fi_unit2|A|2025_11_6_15_24_13']?.play();
	});
</script>

<T.PerspectiveCamera makeDefault fov={15} position={[5, 0, 8]}>
	<OrbitControls
		autoRotate
		autoRotateSpeed={10}
		enableDamping
		enableZoom={false}
		target={[0, 1, 0]}
		enableRotate={false}
	/>
</T.PerspectiveCamera>

<!-- Add lighting here -->
<T.AmbientLight intensity={1} />
<T.DirectionalLight position={[10, 10, 5]} intensity={5} />
<T.PointLight position={[-10, -10, -10]} intensity={5} />

{#await gltf then { scene }}
	<T is={scene} />
{/await}
