<script>
  import { _ } from "svelte-i18n";
</script>

<div>
	<h1>{$_("title", { default: "Common questions about the electric vehicles"})}</h1>
	<p class="subtitle">
		<strong>{$_("subtitle", { default: "Answered by Gaia Green Tech" })}</strong>
	</p>
</div>

<style>
	h1 {
		position: absolute;
		top: 3.57cm;
		left: 21.2cm;
		font-size: 13mm;
		line-height: 1.1;
		width: 80mm;
	}
	.subtitle {
		position: absolute;
		top: 11.15cm;
		left: 21.2cm;
		font-size: 10pt;
	}
</style>