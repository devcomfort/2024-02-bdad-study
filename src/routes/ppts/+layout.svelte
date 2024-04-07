<script lang="ts">
	import { onMount } from 'svelte';

	// Reveal.js
	import Reveal from 'reveal.js';
	// Reveal.js Styles
	import 'reveal.js/dist/reveal.css';
	import 'reveal.js/dist/theme/black.css';
	// Reveal.js Built-in Plugins
	import Highlight from 'reveal.js/plugin//highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';


	onMount(function () {
		const deck = new Reveal({
			plugins: [Highlight, Notes]
		});

		deck.initialize({
			dependencies: []
		});
	});
</script>

<div class="reveal">
	<div class="slides">
		<slot />
	</div>
</div>
