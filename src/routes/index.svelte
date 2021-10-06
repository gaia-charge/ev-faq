<script>
	import { init, register, isLoading } from 'svelte-i18n';
	import Page1 from '../components/Page1.svelte';
	import Page2 from '../components/Page2.svelte';
	import Page3 from '../components/Page3.svelte';
	import Page4 from '../components/Page4.svelte';
	import Page5 from '../components/Page5.svelte';
	import Page6 from '../components/Page6.svelte';
	import environment from '../services/environment';

	const fallbackLocale = 'en';

	register('en', () => import('../services/messages/en.json'));
	register('es', () => import('../services/messages/es.json'));
	register('pl', () => import('../services/messages/pl.json'));
	init({
		fallbackLocale,
		initialLocale: environment.language || fallbackLocale
	});
</script>

{#if !$isLoading}
	<div class="side" id="side-a">
		<img src="/side-a.svg" class="background" />
		<!-- <img src="/side-a.png" class="debug" /> -->
		<Page5 />
		<Page6 />
		<Page1 />
	</div>
	<div class="side" id="side-b">
		<Page2 />
		<Page3 />
		<Page4 />
	</div>
{/if}

<style>
	/*
		With bleed: 307mm x 220mm
		Without: 297mm x 210mm (A4)
	*/
	.side {
		width: 307mm;
        height: 220mm;
        display: grid;
  		grid-template-columns: repeat(3, 1fr);
		position: relative;
	}
	img {
		position: absolute;
	}
	.background {
		width: 307mm;
        height: 220mm;
		z-index: -1000;
	}
	.debug {
		width: 307mm;
        height: 220mm;
		opacity: 0.5;
	}
</style>