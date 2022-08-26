<template>
	<main>
		<div class="c-text-container">
			<h1>Textured Gradients</h1>
			<h2>104</h2>
		</div>
		<div class="c-grad__wrapper">
			<div class="c-grad-container">
				<div class="c-grad c-grad--1"></div>
				<code>		 background: radial-gradient(circle at 65% 35%, rgba(0, 0, 0, 0), mediumblue), url(https://grainy-gradients.vercel.app/noise.svg);    
  		filter: contrast(120%) brightness(100%);</code>
				<p><span>Fig b</span><span>Radial Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--2"></div>
				<code>background: linear-gradient(to right, red, transparent),
		    url(https://grainy-gradients.vercel.app/noise.svg);
		  filter: contrast(170%) brightness(300%);</code>
				<p><span>Fig c</span><span>Conic Gradient</span></p>
			</div>
		</div>
	</main>
</template>

<style scoped lang="scss">
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
	.c-grad {
		min-height: 50vw;
		display: flex;
		flex-direction: column;
		align-items: centre;
	}
	.c-grad--1 {
		 background: radial-gradient(circle at 65% 35%, rgba(0, 0, 0, 0), mediumblue), url(https://grainy-gradients.vercel.app/noise.svg);    
  		filter: contrast(120%) brightness(100%);
	}
	.c-grad--2 {
		  background: linear-gradient(to right, red, transparent),
		    url(https://grainy-gradients.vercel.app/noise.svg);
		  filter: contrast(170%) brightness(300%);
	}

</style>