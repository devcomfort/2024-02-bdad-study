<script lang="ts">
	// Google Fonts
	import GoogleFont, { getFontStyle } from '@svelte-web-fonts/google';
	import type { GoogleFontFamily, GoogleFontVariant } from '@svelte-web-fonts/google';

	// TailwindCSS
	import '../app.pcss';
	import '../tailwind.css';

	const font = {
		family: 'Noto Sans KR' as GoogleFontFamily,
		variants: ['400'] as GoogleFontVariant[]
	} as const;
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="" />
	<GoogleFont fonts={[font]} display="swap" />
</svelte:head>

<div class="h-full w-full" style={getFontStyle(font.family, font.variants[0])}>
	<slot />
</div>
