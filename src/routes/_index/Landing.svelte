<script>
	import GradientBlob from '$lib/components/GradientBlob.svelte'
</script>

<div class="Landing">
	<div id="blobsCenter">
		<GradientBlob width={200} height={250} color={'#1F5EFF'} blur={100} top="-50px" left="0px" />
		<GradientBlob width={250} height={200} color={'#4BFF47'} blur={100} top="50px" left="-60px" />
		<GradientBlob width={220} height={220} color={'#FF30EA'} blur={100} top="50px" left="60px" />
	</div>

	<div id="blobsLeft">
		<GradientBlob width={150} height={150} color={'#4BFF47'} blur={300} />
		<GradientBlob width={150} height={150} color={'#1F5EFF'} blur={300} />
		<GradientBlob width={150} height={150} color={'#FF30EA'} blur={300} />
	</div>

	<div id="blobsRight">
		<GradientBlob width={200} height={200} color={'#4BFF47'} blur={300} />
		<GradientBlob width={200} height={200} color={'#FF30EA'} blur={300} />
		<GradientBlob width={200} height={200} color={'#1F5EFF'} blur={300} />
	</div>

	<h1 id="name">
		Valentin, Junior <br />
		Webdesigner ?
	</h1>

	<p id="since">
		Valentin <br />
		Since 2022
	</p>

	<p id="jobs">
		Webdesigner <br />
		Logodesigner <br />
		And more
	</p>

	<p id="contact">
		I'm free if you <br />
		want a design
	</p>
</div>

<style>
	#name {
		position: absolute;
		top: 40%;
		left: 50%;
		transform: translate(-50%, -50%);
		font-size: 4rem;
		font-style: italic;
		text-transform: uppercase;
		color: #fff;
		white-space: nowrap;
	}

	#blobsCenter {
		position: absolute;
		z-index: 1;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		mix-blend-mode: difference;
		filter: blur(100px);
	}

	#blobsLeft {
		opacity: 0.3;
		position: absolute;
		top: 40%;
		margin-left: 8rem;
		transform: translate(-50%, -50%);
	}
	p {
		position: absolute;
		z-index: 1;
		text-transform: uppercase;
		color: #fff;
		opacity: 0.15;
		font-size: 1.25rem;
	}

	#since {
		top: 33%;
	}

	#jobs {
		top: 48%;
	}

	#contact {
		right: 10%;
		bottom: 20%;
	}

	#blobsRight {
		opacity: 0.3;
		position: absolute;
		bottom: 24%;
		right: 15%;
		transform: translate(-50%, -50%);
	}
</style>
