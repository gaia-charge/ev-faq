<script>
  import { _ } from "svelte-i18n";
</script>

<div>
	<h2>{$_("charge-duration.title", { default: "How long does it take to charge?"})}</h2>
	<div class="lead">
		<p>
			{$_("charge-duration.lead", {
			default:
				"This depends on a model of the car and the charger's output but here are example charging times for VW ID.3 Pro"
			})}
			<sup>3)</sup>
		</p>
	</div>
	{$_("charge-duration.charging-point", {
	default:
		"Charging point"
	})}
	{$_("charge-duration.power", {
	default:
		"Power"
	})}
	{$_("charge-duration.time-to-charge", {
	default:
		"Time to charge"
	})}
	{$_("charge-duration.rate-of-charge", {
	default:
		"Rate of charge"
	})}
	{$_("charge-duration.charging-point", {
	default:
		"{fromPercent}% to {toPercent}% in {minutes} minutes"
	})}
</div>

<div>
	<h2>{$_("cost.title", { default: "How much does it cost to run?"})}</h2>
	<div class="lead">
		<p>
			{$_("cost.lead", {
			default:
				"Compared to gasoline and diesel cars, EV's are much cheaper to run"
			})}
		</p>
	</div>
	{$_("cost.gasoline", {
	default:
		"VW Golf gasoline"
	})}  <sup>4)</sup>

	{$_("cost.diesel", {
	default:
		"VW Golf diesel"
	})}

	{$_("cost.public-charging", {
	default:
		"VW ID.3 public charging"
	})}

	{$_("cost.home-charging", {
	default:
		"VW ID.3 home charging"
	})}

	{$_("cost.free-charging", {
	default:
		"VW ID.3 free and solar energy"
	})}

	{$_("cost.consumption-per-100km", {
	default:
		"Consumption per 100km"
	})}

	{$_("cost.cost-per-100km", {
	default:
		"Cost per 100km"
	})} <sup>5)</sup> <sup>6)</sup> <sup>7)</sup> <sup>8)</sup>

	{$_("cost.annual-savings", {
	default:
		"Annual savings"
	})} <sup>9)</sup>
</div>

<style>
	div {
		background-color: blue;
	}
</style>
