<script>
	let dogImage = {
		src: 'images/dog.jpg',
		alt: 'Picture of a black and white dog',
		tagline: 'Adopt, don\'t shop!'
	}
</script>

<main>
	<h1>Dog Shelter</h1>
	<h2>{dogImage.tagline}</h2>
	<img src={dogImage.src} alt={dogImage.alt} width="100%" />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>