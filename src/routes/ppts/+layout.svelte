<script lang="ts">
	import { onMount } from 'svelte';

	// Google Fonts
	import GoogleFont, { getFontStyle } from '@svelte-web-fonts/google';
	import type { GoogleFontFamily, GoogleFontVariant } from '@svelte-web-fonts/google';

	// Reveal.js
	import Reveal from 'reveal.js';
	// Reveal.js Styles
	import 'reveal.js/dist/reveal.css';
	import 'reveal.js/dist/theme/black.css';
	// Reveal.js Built-in Plugins
	import Highlight from 'reveal.js/plugin//highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';

	const font = {
		family: 'Noto Sans KR' as GoogleFontFamily,
		variants: ['400'] as GoogleFontVariant[]
	} as const;

	onMount(function () {
		const deck = new Reveal({
			plugins: [Highlight, Notes]
		});

		deck.initialize({
			dependencies: []
		});
	});
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="" />
	<GoogleFont fonts={[font]} display="swap" />
</svelte:head>

<div class="reveal" style={getFontStyle(font.family, font.variants[0])}>
	<div class="slides">
		<slot />
	</div>
</div>
