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
	div {
		background-color: red;
	}
</style>
