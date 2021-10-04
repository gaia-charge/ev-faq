<script>
  import { _ } from "svelte-i18n";
</script>

<div>
	<h2>{$_("battery.title", { default: "How long does the battery last?"})}</h2>
	<div class="lead">
		<p>
			{$_("battery.lead", { default: "Most manufacturers guarantee at least <strong>{percent}% capacity after {mileage}km</strong>",
			values: { percent: 70, mileage: "160.000"} })} <sup>16)</sup>
			{$_("battery.lead2", { default: "and according to study by Nissan, the <strong>batteries will outlast the vehicle itself by 10-12 years</strong>" })} <sup>17)</sup>.
			{$_("battery.lead3", { default: "After that time the batteries can be reused as energy storage in houses and after that up to <strong>{percent}% of materials in batteries can be recycled</strong>",
			values: { percent: 93 } })} <sup>18)</sup>.
		</p>
	</div>
	{$_("battery.lifespan.car", { default: "<strong>{percent}%</strong> after {mileage}km",
	values: { percent: 70, mileage: "160.000"} })}

	{$_("battery.lifespan.home", { default: "<strong>{years}</strong> years after the car",
	values: { years: 10 } })}

	{$_("battery.lifespan.recycle", { default: "<strong>{percent}%</strong> recyclable",
	values: { percent: 93 } })}	
</div>

<div>
	<h2>{$_("charging-alternatives.title", { default: "I have a shared garage or park off the street. Can I still charge my car?"})}</h2>
	<div class="lead">
		<p>
			{$_("charging-alternatives.lead", { default: "The rules depend on a country but usually you're able to install a home charger in a shared garage, as long as it has a separate meter from the communal one" })}.
			{$_("charging-alternatives.lead2", { default: "The cost of the installation is on you, but many car manufacturers include a wall charger as a free perk. <strong>Cost of a home charger is around {price}€</strong> plus installation",
			values: { price: 500 } })}.
			{$_("charging-alternatives.lead3", { default: "If you don't have a garage, some cities offer off the street charging, but even without it, you should be able to charge the car enough, just by using the public chargers during your daily errands." })}.
		</p>
	</div>
</div>

<style>
	div {
		background-color: magenta;
	}
</style>
