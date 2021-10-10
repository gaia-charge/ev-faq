<script>
  import { _ } from "svelte-i18n";
</script>

<div class="page">
	<div id="charge-duration">
		<h3>{$_("charge-duration.title", { default: "How long does it take to charge?"})}</h3>
		<div class="lead">
			<p>
				{$_("charge-duration.lead", {
				default:
					"This depends on a model of the car and the charger's output but here are example charging times for Hyundai IONIQ 5"
				})}:
				<sup>3)</sup>
			</p>
		</div>
		<table>
			<tr>
				<th style="width: 22.5mm">{$_("charge-duration.charging-point", { default: "Charging point" })}</th>
				<th style="width: 14mm">{$_("charge-duration.power", { default: "Power" })}</th>
				<th style="width: 22.5mm">{$_("charge-duration.time-to-charge", { default: "Time to charge" })}</th>
				<th>{$_("charge-duration.rate-of-charge", { default: "Rate of charge" })}</th>
			</tr>
			<tr>
				<td><img src="/wall-socket.svg" alt="Wall Socket" /></td>
				<td>2,3kW</td>
				<td>37h</td>
				<td>1h = +10km</td>
			</tr>
			<tr>
				<td><img src="/home-charger.svg" alt="Home Charger" /></td>
				<td>3,7kW</td>
				<td>23h</td>
				<td>1h = +17km</td>
			</tr>
			<tr>
				<td><img src="/public-charger.svg" alt="Public Charger" /></td>
				<td>11kW</td>
				<td>7h45m</td>
				<td>1h = +50km</td>
			</tr>
			<tr>
				<td><img src="/fast-charger.svg" alt="Fast Charger" /></td>
				<td>50kW</td>
				<td>
					{@html $_("charge-duration.percent-in-minutes", {
					default: "{fromPercent}% to {toPercent}% in<br />{minutes}min",
					values: { fromPercent: 10, toPercent: 80, minutes: 64 }
					})}
				</td>
				<td>1h = +250km</td>
			</tr>
			<tr>
				<td><img src="/super-fast-charger.svg" alt="Super Fast Charger" /></td>
				<td>175kW</td>
				<td>
					{@html $_("charge-duration.percent-in-minutes", {
					default: "{fromPercent}% to {toPercent}% in<br />{minutes}min",
					values: { fromPercent: 10, toPercent: 80, minutes: 23 }
					})}
				</td>
				<td>1h = +700km</td>
			</tr>
		</table>
	</div>
	
	<div id="cost">
		<h3>{$_("cost.title", { default: "How much does it cost to run?"})}</h3>
		<div class="lead">
			<p>
				{$_("cost.lead", {
				default:
					"Compared to gasoline and diesel cars, EV's are much cheaper to run"
				})}:
			</p>
		</div>
		<table>
			<tr>
				<th style="width: 20mm"></th>
				<th style="width: 12mm">{$_("cost.gasoline", { default: "VW Golf gasoline" })} <sup>4)</sup></th>
				<th style="width: 12mm">{$_("cost.diesel", { default: "VW Golf diesel" })}</th>
				<th style="width: 12mm">{$_("cost.public-charging", { default: "VW ID.3 public charging" })}</th>
				<th style="width: 12mm">{$_("cost.home-charging", { default: "VW ID.3 home charging" })}</th>
				<th style="width: 17mm">{$_("cost.free-charging", { default: "VW ID.3 free and solar energy" })}</th>
			</tr>
			<tr style="height: 13.7mm">
				<td class="header">{$_("cost.consumption-per-100km", { default: "Consumption per 100km" })}</td>
				<td>6.28L</td>
				<td>5.9L</td>
				<td>16.6kW</td>
				<td>16.6kW</td>
				<td>16.6kW</td>
			</tr>
			<tr style="height: 10.7mm">
				<td class="header">{$_("cost.cost-per-100km", { default: "Cost per 100km" })}</td>
				<td>9.1&euro;<sup>5)</sup></td>
				<td>7.86&euro;<sup>6)</sup></td>
				<td>5.81&euro;<sup>7)</sup></td>
				<td>0.58&euro;<sup>8)</sup></td>
				<td>0&euro;</td>
			</tr>
			<tr style="height: 12mm">
				<td class="header">{$_("cost.annual-savings", { default: "Annual savings" })} <sup>9)</sup></td>
				<td>{$_("not-available", { default: "n/a" })}</td>
				<td>+124&euro;</td>
				<td>+329&euro;</td>
				<td>+852&euro;</td>
				<td>+910&euro;</td>
			</tr>
		</table>
	</div>
</div>

<style>
	h3 {
		position: absolute;
		left: 113mm;
		width: 8.2cm;
	}
	#charge-duration h3 {
		top: 14mm;
	}
	#charge-duration .lead {
		position: absolute;
		left: 113mm;
		top: 31mm;
		width: 8.2cm;
	}

	#charge-duration table {
		position: absolute;
		left: 111mm;
		top: 44mm;
		width: 8.4cm;
	}

	#charge-duration th {
		color: #EDF8FB;
		font-size: 2.6mm;
		font-weight: 800;
		font-family: 'Inter';
		height: 6mm;
    	padding-bottom: 1.5mm;
	}

	#charge-duration td {
		color: #008B8C;
		text-align: center;
		font-size: 3.1mm;
    	height: 10.7mm;
	}

	#charge-duration td img {
		width: 9mm;
	}


	#cost h3 {
		top: 109mm;
	}

	#cost .lead {
		position: absolute;
		left: 113mm;
		top: 126mm;
		width: 8.2cm;
	}

	#cost table {
		position: absolute;
		left: 110mm;
		top: 137mm;
	}

	#cost th {
		color: #EDF8FB;
		font-size: 2.3mm;
		font-weight: 800;
		font-family: 'Inter';
		height: 6mm;
    	padding: 1.5mm 0;
	}

	#cost td {
		color: #008B8C;
		text-align: center;
		font-size: 3.1mm;
	}

	#cost td.header {
		font-weight: 800;
		font-family: 'Inter';
		font-size: 2.6mm;
	}
</style>
