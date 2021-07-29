<script lang="ts">
	export let name: string;
	import Counter from './Counter.svelte';
  const p = {
		count: 20000,
		isHello: true,
		cats: [
			{ id: 'J---aiyznGQ', name: 'Keyboard Cat' },
			{ id: 'z_AbfPXTKms', name: 'Maru' },
			{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
		]
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>
<Counter {...p} />

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
