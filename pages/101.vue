<template>
	<main>
		<div class="c-text-container">
			<h1>Introduction to Gradients</h1>
			<h2>101</h2>
		</div>
		<div class="c-grad__wrapper">
			<div class="c-grad-container">
				<div class="c-grad c-grad--linear">
					</div>
				<code>
					background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(255,255,255,1) 100%);
				</code>
				<p><span>Fig a</span><span>Linear Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--radial"></div>
				<code>background: radial-gradient(yellow, #009966, purple);</code>
				<p><span>Fig b</span><span>Radial Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--conic"></div>
				<code>background: conic-gradient(red, orange, yellow, green, blue);</code>
				<p><span>Fig c</span><span>Conic Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--repeating"></div>
				<code>background: repeating-linear-gradient(red, yellow 25%);</code>
				<p><span>Fig c</span><span>Linear Repeating Gradient</span></p>
			</div>
		</div>
	</main>
</template>
<style scoped lang="scss">
	main {

	}
	.c-text-container {
		text-align: center;
	}
	.c-grad__wrapper {
		display: grid;
		grid-template-columns: repeat(12, [col-start] 1fr);
		gap: 3vw;
		padding: 3vw;
	}
	.c-grad-container {
		grid-column: 3 / span 8;
		font-family: monospace;
		p, code {
			display: flex;
			justify-content: space-between;
			border-bottom: 1px solid rgba(black, 0.35);
		}
	}
	style {
	  white-space:pre-wrap; 
	  display:block;
	  outline:none;
	  text-align: center;
	  margin-top:4em;
	  mix-blend-mode: difference;
	}
	.c-grad {
		min-height: 50vw;
		display: flex;
		flex-direction: column;
		align-items: centre;
		&--linear {
			background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(255,255,255,1) 100%);
		}
		&--radial {
			background: radial-gradient(yellow, #009966, purple);
		}
		&--conic {
			background: conic-gradient(red, orange, yellow, green, blue);
		}
		&--repeating {
			background: repeating-linear-gradient(red, yellow 25%);
		}
	}
</style>