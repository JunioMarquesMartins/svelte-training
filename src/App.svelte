<script>
	import MAinHeader from '../src/Components/Header/MAinHeader.svelte';
	import Button from '../src/Components/atoms/Button/Button.svelte';
	export let name;
	let surname = "Print String";

	let srcImage = '/images/rick.gif';
	let titleImage = 'Rick Astley';

	// Render HTML
	let stringHTML = `this string contains some <strong>HTML!!!</strong>`;
</script>

<main>
	<MAinHeader/>
	<h1>Hello {name}!</h1>
	<p>{surname.toUpperCase()}</p>
	<img src={srcImage} alt="{titleImage} dances." />

	<!-- Render HTML -->
	<p>{@html stringHTML}</p>

	<Button/>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
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

	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>