<script>
  import { _ } from "svelte-i18n";
</script>

<div class="page">
	<div id="battery">
		<h3>{$_("battery.title", { default: "How long does the battery last?"})}</h3>
		<div class="lead">
			<p>
				{@html $_("battery.lead", { default: "Most manufacturers guarantee at least <strong>{percent}% capacity after {mileage}km</strong>",
				values: { percent: 70, mileage: "160.000"} })} <sup>11)</sup>
				{@html $_("battery.lead2", { default: "and according to study by Nissan, the <strong>batteries will outlast the vehicle itself by 10-12 years</strong>" })} <sup>12)</sup>.
				{@html $_("battery.lead3", { default: "After that time the batteries can be reused as energy storage in houses and after that up to <strong>{percent}% of materials in batteries can be recycled</strong>",
				values: { percent: 93 } })} <sup>13)</sup>.
			</p>
		</div>

		<div class="flow">
			<span class="step" id="car">
				{@html $_("battery.lifespan.car", { default: "<strong>{percent}%</strong> after {mileage}km",
				values: { percent: 70, mileage: "160.000"} })}
			</span>
			<span class="step" id="home">
				{@html $_("battery.lifespan.home", { default: "<strong>{years}</strong> years after the car",
				values: { years: 10 } })}
			</span>
			<span class="step" id="recycle">
				{@html $_("battery.lifespan.recycle", { default: "<strong>{percent}%</strong> recyclable",
				values: { percent: 93 } })}
			</span>
		</div>
	</div>
	
	<div id="charging-alternatives">
		<h3>{$_("charging-alternatives.title", { default: "I have a shared garage or park off the street. Can I still charge my car?"})}</h3>
		<div class="lead">
			<p>
				{$_("charging-alternatives.lead", { default: "The rules depend on a country but usually you're able to install a home charger in a shared garage, as long as it has a separate meter from the communal one" })}.
				{@html $_("charging-alternatives.lead2", { default: "The cost of the installation is on you, but many car manufacturers include a wall charger as a free perk. <strong>Cost of a home charger is around {price}€</strong> plus installation",
				values: { price: 500 } })}.
				{$_("charging-alternatives.lead3", { default: "If you don't have a garage, some cities offer off the street charging, but even without it, you should be able to charge the car enough, just by using the public chargers during your daily errands." })}.
			</p>
		</div>
	</div>
</div>

<style>
	h3 {
		position: absolute;
		left: 1.3cm;
		font-size: 5.9mm;
		line-height: 1.35;
		width: 8.2cm;
	}
	#battery h3 {
		top: 1.45cm;
	}
	#battery .lead {
		left: 1.3cm;
		top: 3.25cm;
		width: 8.2cm;
	}
	.flow {
    	color: #008B8C;
		font-size: 10pt;
		font-weight: 1000;
		line-height: 1.1;
	}
	.flow span {
		position: absolute;
		width: 2.3cm;
		text-align: center;
		top: 9cm;
	}
	#car {
		left: 15mm;
	}
	#home {
		left: 45mm;
	}
	#recycle {
		left: 73mm;
	}
	#charging-alternatives h3 {
		top: 10.6cm;
	}
	#charging-alternatives .lead {
		left: 1.4cm;
		top: 13.25cm;
		width: 8.2cm;
	}
</style>
