<script>
  import { _ } from "svelte-i18n";
</script>

<div>
	<h2>{$_("contact.title", { default: "Contact us!"})}</h2>
	<div class="lead">
		<p>
			{$_("contact.lead", { default: "See all the footnotes and the up-to-date version of this ﬂyer at" })}:
		</p>
	</div>
</div>>

<style>
	div {
		background-color: yellow;
	}
</style>
