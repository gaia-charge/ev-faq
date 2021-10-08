<script>
  import { _ } from "svelte-i18n";
</script>

<div class="page">
	<div id="range">
		<h3>{$_("range.title", { default: "What's the range of an EV?"})}</h3>
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
		<div class="ticks">
			<div class="tick-150">
				{$_("range.tick", {
				default:
					"{percent}% of cars has {range}km of range",
					values: { percent: 98, range: 150 }
				})}
			</div>
			<div class="tick-250">
				{$_("range.tick", {
				default:
					"{percent}% of cars has {range}km of range",
					values: { percent: 80, range: 250 }
				})}
			</div>
			<div class="tick-350">
				{$_("range.tick", {
				default:
					"{percent}% of cars has {range}km of range",
					values: { percent: 48, range: 350 }
				})}
			</div>
			<div class="tick-400">
				{$_("range.tick", {
				default:
					"{percent}% of cars has {range}km of range",
					values: { percent: 24, range: 400 }
				})}
			</div>
		</div>
	</div>
	
	<div id="charge-frequency">
		<h3>{$_("charge-frequency.title", { default: "How often do I need to charge it then?"})}</h3>
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
</div>

<style>
	h3 {
		position: absolute;
		left: 13mm;
	}
	#range h3 {
		top: 14mm;
	}
	#range .lead {
		position: absolute;
		left: 13mm;
		top: 24mm;
		width: 8.2cm;
	}
	.ticks div {
		position: absolute;
   		color: #008B8C;
		font-size: 3.5mm;
		line-height: 1.05;
	}
	.tick-150 {
		left: 15mm;
		top: 53mm;
		width: 20mm;
	}
	.tick-250 {
		left: 17mm;
		top: 41mm;
		width: 27mm;
	}
	.tick-350 {
		left: 53mm;
		top: 35mm;
		width: 30mm;
	}
	.tick-400 {
		left: 72mm;
		top: 49mm;
		width: 26mm;
	}
	#charge-frequency h3 {
		top: 90mm;
		width: 8.2cm;
	}
	#charge-frequency .lead {
		position: absolute;
		left: 13mm;
		top: 108mm;
		width: 8.2cm;
	}
</style>
