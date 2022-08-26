<template>
	<main>
		<h1>Gradient Worksheet</h1>
		<div class="c-card-container">
			<NuxtLink to="/101" class="c-card">
				<div>
					<h2>1.01</h2>
					<h3>Introduction to Gradients</h3>
				</div>
			</NuxtLink>
			<div class="c-card">
				<h2>1.02</h2>
				<h3>Layered Gradient Backgrounds</h3>
			</div>
			<div class="c-card">
				<h2>1.03</h2>
				<h3>Stepped Gradients</h3>
			</div>
			<div class="c-card">
				<h2>1.04</h2>
				<h3>Adding Texture</h3>
			</div>
		</div>
	</main>
</template>

<style scoped lang="scss">
main {
	min-height: 100vh;
	background-image: linear-gradient(
	  45deg,
	  hsl(0deg 100% 56%) 0%,
	  hsl(26deg 100% 50%) 16%,
	  hsl(38deg 100% 50%) 25%,
	  hsl(50deg 100% 50%) 32%,
	  hsl(61deg 100% 47%) 38%,
	  hsl(73deg 100% 48%) 44%,
	  hsl(93deg 96% 57%) 50%,
	  hsl(136deg 100% 52%) 56%,
	  hsl(176deg 100% 43%) 61%,
	  hsl(200deg 100% 50%) 67%,
	  hsl(216deg 100% 50%) 72%,
	  hsl(257deg 100% 50%) 78%,
	  hsl(269deg 100% 49%) 84%,
	  hsl(278deg 100% 48%) 90%,
	  hsl(285deg 98% 48%) 100%
	);
}

.c-card-container {
	display: grid;
	grid-template-columns: repeat(12, [col-start] 1fr);
	gap: 3vw;
	margin: 3vw;
}

.c-card {
	grid-column: auto / span 6;
	padding: 10vw;
	display: flex;
	flex-direction: column;
	align-items: center;
	background: black;
	color: white;
	border-radius: 999px;
	text-align: center;
	transition: all 650ms ease;
	&:hover,
	&:active,
	&:focus {
		border-radius: 0;
	}
}
</style>