<script>
	import Landing from './_index/Landing.svelte'

	import logoPng from '$lib/assets/logo.png'
</script>

<main>
	<img src={logoPng} alt="" id="logo" />

	<Landing />
</main>

<style>
	:global(body) {
		margin: 0;
		background-color: #212121;
		font-family: 'Rubik', sans-serif;
		padding-left: 4.5rem;
	}

	#logo {
		position: absolute;
		top: 2rem;
		left: 50%;
		transform: translateX(-50%);
	}
</style>
