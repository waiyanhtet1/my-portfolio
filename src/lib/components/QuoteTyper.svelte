<script lang="ts">
	let quotes = [
		'In the cyber-future, robots won’t replace us — they’ll upgrade what we can imagine.',
		'A robotic world isn’t about metal and code; it’s about humans unlocking new levels of possibility.',
		'The future belongs to those who can think beyond the circuit and dream beyond the screen.'
	];

	let displayText = '';
	let quoteIndex = 0;

	const typeSpeed = 40;
	const holdTime = 1800;

	async function typeQuote(text: string) {
		displayText = '';
		for (let char of text) {
			displayText += char;
			await new Promise((r) => setTimeout(r, typeSpeed));
		}
	}

	async function startLoop() {
		while (true) {
			await typeQuote(quotes[quoteIndex]);
			await new Promise((r) => setTimeout(r, holdTime));
			quoteIndex = (quoteIndex + 1) % quotes.length;
		}
	}

	startLoop();
</script>

<p class="quote">{displayText}</p>

<style>
	.quote {
		position: absolute;
		top: 0;
		left: 0;
		color: white;
		padding: 30px 20px;
		letter-spacing: 1px;
		z-index: -999;
		font-family: var(--secondary-font);
		text-transform: uppercase;
		font-size: 18px;
		width: 600px;
	}
</style>
