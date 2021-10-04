<script>
  import { _ } from "svelte-i18n";
</script>

<div>
	<h2>{$_("advantages.title", { default: "What are things only EV's can do?"})}</h2>
	<div class="lead">
		<p>
			{$_("advantages.lead", { default: "There are some technical advantages of EV's that simply can't be matched by petrol or diesel cars" })}
		</p>
	</div>
	
	{$_("advantages.torque.title", { default: "Instant torque" })}
	{$_("advantages.torque.lead", { default: "The electric motor delivers the acceleration instantly, making you first on any stop light" })}
	{$_("advantages.ac.title", { default: "Scheduling the AC" })}
	{$_("advantages.ac.lead", { default: "EVs allow you to schedule warming up or cooling of the car remotely so you always enter the car with the temperature you like" })}
	{$_("advantages.quiet.title", { default: "Incredibly quiet" })}
	{$_("advantages.quiet.lead", { default: "EVs don't disturb neighbours, they won't wake up babies and even at highway speeds you can have a conversation with your regular voice" })}
	{$_("advantages.pollution.title", { default: "Zero pollution" })}
	{$_("advantages.pollution.lead", { default: "If you're ecology conscious, this one is for you. No tailpipe, no emissions. Even including the pollution from the dirtiest electricity sources, EVs still outperform petrol/diesel cars" })} <sup>12)</sup>
	{$_("advantages.benefits.title", { default: "Additional benefits" })}
	{$_("advantages.benefits.lead", { default: "In some countries/regions, EVs have additional benefits like free parking, ability to use bus lanes, enter congestion zones without a charge and most chargers in supermarkets and shopping centres are located very close to the entrance" })}
</div>

<style>
	div {
		background-color: cyan;
	}
</style>
