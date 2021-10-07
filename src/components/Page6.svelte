<script>
  import { _, locale } from "svelte-i18n";
</script>

<div class="page">
	<h2>{$_("contact.title", { default: "Contact us!"})}</h2>
	<div class="social facebook">
		@{$_("contact.facebook", { default: "GaiaGreenTechES"})}
	</div>
	<div class="social instagram">
		@{$_("contact.instagram", { default: "GaiaGreenTechESP"})}
	</div>
	<div class="social twitter">
		@{$_("contact.twitter", { default: "Gaia_Green_Tech"})}
	</div>
	<div class="lead">
		<p>
			{$_("contact.lead", { default: "See all the footnotes and the up-to-date version of this ﬂyer at" })}:<br />
			https://ggrn.link/ev-faq
			<!--
				QR Code made with https://qr-code-generator.org/
				Colors:
					Transparent background
					Foreground: #4c8c40
				Design:
					Marked border: 14
					Marker center: 6
				Logo:
					File: green_two_color@8x.png
					Logo size: 80%
				Options:
					Size: 800
					Precision: Q - High
				Extras:
					Add fill="#98c93f" to the three markers
			-->
			<img src="/qrcode-ev-faq-{$locale}.svg" alt="QR Code" class="qr" />
		</p>
	</div>
</div>

<style>
	h2 {
		position: absolute;
		left: 114mm;
		top: 36mm;
		font-size: 10mm;
	}
	.social {
		position: absolute;
		left: 113mm;
    	font-size: 3.9mm;
    	color: #008B8C;
	}
	.facebook {
		top: 56mm;
	}
	.instagram {
		top: 70mm;
	}
	.twitter {
		top: 84mm;
	}
	.lead {
		position: absolute;
		left: 113mm;
		top: 100mm;
		font-size: 3.9mm;
		width: 75mm;
		line-height: 1.2;
	}
	.qr {
		position: absolute;
		top: 20mm;
		left: 0mm;
		width: 32mm;
	}
</style>
