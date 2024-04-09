<script lang="ts">
	import { onMount, onDestroy } from 'svelte';

	// Reveal.js
	import Reveal from 'reveal.js';
	// Reveal.js Styles
	import 'reveal.js/dist/reveal.css';
	import 'reveal.js/dist/theme/black.css';
	// Reveal.js Built-in Plugins
	import Highlight from 'reveal.js/plugin/highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';

	let deck: Reveal.Api;

	onMount(function () {
		deck = new Reveal({
			plugins: [Highlight, Notes]
		});

		deck.initialize({
			dependencies: []
		});
	});

	onDestroy(function () {
		deck.destroy();
	});
</script>

<svelte:head>
	<link
		rel="stylesheet"
		href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/styles/dark.min.css"
	/>
</svelte:head>

<div class="reveal">
	<div class="slides">
		<slot />
	</div>
</div>
