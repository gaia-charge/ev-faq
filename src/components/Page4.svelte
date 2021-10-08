<script>
  import { _ } from "svelte-i18n";
</script>

<div class="page">
	<h3>{$_("advantages.title", { default: "What are things only EV's can do?"})}</h3>
	<div class="lead">
		<p>
			{$_("advantages.lead", { default: "There are some technical advantages of EV's that simply can't be matched by petrol or diesel cars" })}
		</p>
	</div>
	
	<div class="advantage torque">
		<h4>{$_("advantages.torque.title", { default: "Instant torque" })}</h4>
		<p>{$_("advantages.torque.lead", { default: "The electric motor delivers the acceleration instantly, making you first on any stop light" })}</p>
	</div>
	<div class="advantage ac">
		<h4>{$_("advantages.ac.title", { default: "Scheduling the AC" })}</h4>
		<p>{$_("advantages.ac.lead", { default: "EVs allow you to schedule warming up or cooling of the car remotely so you always enter the car with the temperature you like" })}</p>
	</div>
	<div class="advantage quiet">
		<h4>{$_("advantages.quiet.title", { default: "Incredibly quiet" })}</h4>
		<p>{$_("advantages.quiet.lead", { default: "EVs don't disturb neighbours, they won't wake up babies and even at highway speeds you can have a conversation with your regular voice" })}</p>
	</div>
	<div class="advantage pollution">
		<h4>{$_("advantages.pollution.title", { default: "Zero pollution" })}</h4>
		<p>{$_("advantages.pollution.lead", { default: "If you're ecology conscious, this one is for you. No tailpipe, no emissions. Even including the pollution from the dirtiest electricity sources, EVs still outperform petrol/diesel cars" })} <sup>12)</sup></p>
	</div>
	<div class="advantage benefits">
		<h4>{$_("advantages.benefits.title", { default: "Additional benefits" })}</h4>
		<p>{$_("advantages.benefits.lead", { default: "In some countries/regions, EVs have additional benefits like free parking, ability to use bus lanes, enter congestion zones without a charge and most chargers in supermarkets and shopping centres are located very close to the entrance" })}</p>
	</div>
</div>

<style>
	h3 {
		position: absolute;
		left: 212mm;
		top: 14mm;
		width: 8.2cm;
	}
	.lead {
		position: absolute;
		left: 212mm;
		top: 31mm;
		width: 8.2cm;
	}
	.advantage {
		position: absolute;
		width: 4cm;
	}
	.advantage h4 {
		color: #8FC84E;
		font-family: Inter;
		font-weight: 800;
    	font-size: 3.2mm;
	}
	.advantage p {
    	color: #008B8C;
		font-size: 3.2mm;
		line-height: 1.15;
	}
	.torque {
		left: 212mm;
		top: 58mm;
	}
	.ac {
		left: 254mm;
		top: 58mm;
	}
	.quiet {
		left: 212mm;
		top: 100mm;
	}
	.pollution {
		left: 254mm;
		top: 100mm;
	}
	.benefits {
		left: 212mm;
		top: 145mm;
    	width: 48mm;
	}
</style>