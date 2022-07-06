<script lang="ts">
	import { onMount } from 'svelte'
	import DrawBlob from 'blob-animated'

	export let blob: ConstructorParameters<typeof DrawBlob>[0] | null = null
	export let width: number
	export let height: number
	export let color: string
	export let blur: number
	export let top: string = "0px"
	export let left: string = "0px"

	let canvas: HTMLCanvasElement
	onMount(() => {
		new DrawBlob({
			canvas,
			speed: 90,
			scramble: 0.12,
			color,
			...blob,
		})
	})
</script>

<div
	class="GradientBlob"
	style={`
        width: ${width}px;
        height: ${height}px;
        top: ${top};
        left: ${left};
    `}
>
	<canvas
		style={`transform: scale(${width / 1000}, ${
			height / 1000
		}) translate(50%, 50%); filter: blur(${blur}px)`}
		bind:this={canvas}
	/>
</div>

<style>
	.GradientBlob {
		position: absolute;
		transform: translate(-50%, -50%);
	}

	canvas {
		position: absolute;
		top: -500px;
		left: -500px;
		display: block;
	}
</style>
