<script>
	import Page1 from '../components/Page1.svelte';
	import Page2 from '../components/Page2.svelte';
	import Page3 from '../components/Page3.svelte';
	import Page4 from '../components/Page4.svelte';
	import Page5 from '../components/Page5.svelte';
	import Page6 from '../components/Page6.svelte';
</script>

<div class="side" id="side-a">
	<Page5 />
	<Page6 />
	<Page1 />
</div>
<div class="side" id="side-b">
	<Page2 />
    <Page3 />
    <Page4 />
</div>

<style>
	.side {
		height: 210mm;
		width: 297mm;
		background: -webkit-linear-gradient(0deg, #daf9f9, #daf9f9) !important;
        display: grid;
  		grid-template-columns: repeat(3, 1fr);
	}

	@media screen {
		.side {
			width: calc(100vw - 5em);
            height: calc(100vw * (210/297) - 5em);
			margin: 2em !important;
			border: 0.5em rgba(0, 0, 0, 0.5) solid;
		}
	}
    :global(h1, h2) {
        margin: 0;
    }
</style>