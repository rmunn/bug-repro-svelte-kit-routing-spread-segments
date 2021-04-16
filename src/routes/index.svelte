<script>
	import Links from '$lib/Links.svelte'

	let urls = [
		['/foo/one/two', true],
		['/food/one/two', false],
		['/one-bar/two/three', true],
		['/one-bard/two/three', false],
	]
</script>

<svelte:head>
	<title>Bug repro</title>
</svelte:head>

<main>
	<h1>Bug repro</h1>

	<p>
		Links to demonstrate bug:<br/>
		
		<Links {urls} />
	</p>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4rem;
		font-weight: 100;
		line-height: 1.1;
		margin: 4rem auto;
		max-width: 14rem;
	}

	p {
		max-width: 14rem;
		margin: 2rem auto;
		line-height: 1.35;
	}

	@media (min-width: 480px) {
		h1 {
			max-width: none;
		}

		p {
			max-width: none;
		}
	}
</style>
