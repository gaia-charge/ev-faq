<script>
  import { _ } from "svelte-i18n";
</script>

<div>
	<h2>{$_("range.title", { default: "What's the range of an EV?"})}</h2>
	<div class="lead">
		<p>
			{$_("range.lead", {
			default:
				"More than {percent}% of new EVs have a range of at least {range}km",
				values: { percent: 80, range: 250 }
			})}
			<sup>1)</sup>
		</p>
	</div>
	{$_("range.tick", {
	default:
		"{percent}% of cars has {range}km range",
		values: { percent: 98, range: 150 }
	})}
</div>

<div>
	<h2>{$_("charge-frequency.title", { default: "How often do I need to charge it then?"})}</h2>
	<div class="lead">
		<p>
			{$_("charge-frequency.lead", {
			default:
				"On average, you would need to charge it about every {period}",
				values: { period: "2 weeks" }
			})}
			<sup>2)</sup>
		</p>
	</div>
</div>

<style>
	div {
		background-color: green;
	}
</style>
