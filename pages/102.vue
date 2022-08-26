<template>
	<main>
		<div class="c-text-container">
			<h1>Layered Gradients</h1>
			<h2>102</h2>
		</div>
		<div class="c-grad__wrapper">
			<div class="c-grad-container">
				<div class="c-grad c-grad--1">
				</div>
				<code>
					background: linear-gradient(180deg, #FFFFFF 0%, #000000 100%), linear-gradient(90deg, #FFFFFF 0%, #000000 100%), #FF0000;
					background-blend-mode: multiply, screen, normal;
				</code>
				<p><span>Fig a</span><span>Layered Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--2">
				</div>
				<code>
					background: radial-gradient(65% 100% at 50% 0%, #00FF94 0%, rgba(0, 255, 148, 0.25) 100%), linear-gradient(230deg, #000000 25%, #170059 100%), linear-gradient(215deg, #FFEBB9 10%, #19004E 80%), radial-gradient(100% 245% at 100% 100%, #FFFFFF 0%, #000353 100%), linear-gradient(125deg, #1400FF 0%, #3A0000 100%), linear-gradient(225deg, #00F0FF 30%, #000B6F 45%, #00EBFC 45%, #001676 65%, #00E1F6 65%, #001676 85%, #00ECFD 85%, #001676 100%), linear-gradient(135deg, #00F0FF 0%, #000B6F 15%, #00EBFC 15%, #001676 35%, #00E1F6 35%, #001676 55%, #00ECFD 55%, #001676 100%);
					background-blend-mode: soft-light, screen, overlay, overlay, difference, overlay, normal;
				</code>
				<p><span>Fig b</span><span>Layered Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--3">
				</div>
				<code>
					background: radial-gradient(circle at 50% 50%, #FFFFFF 0%, #000000 100%), conic-gradient(red, yellow, lime, aqua, blue, fuchsia, red);
					background-blend-mode: color-dodge, normal;
				</code>
				<p><span>Fig c</span><span>Layered Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--4">
				</div>
				<code>
					background:
					linear-gradient(-45deg, white 25%, transparent 25%, transparent 75%, black 75%, black) 0 0,
					linear-gradient(-45deg, black 25%, transparent 25%, transparent 75%, white 75%, white) 1em 1em,
					linear-gradient(45deg, black 17%, transparent 17%, transparent 25%, black 25%, black 36%, transparent 36%, transparent 64%, black 64%, black 75%, transparent 75%, transparent 83%, black 83%) 1em 1em;
					background-color: white;
					background-size: 2em 2em;
				</code>
				<p><span>Fig d</span><span>Layered Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--5">
				</div>
				<code>
					background-color:#269;
					background-image: linear-gradient(white 2px, transparent 2px),
					linear-gradient(90deg, white 2px, transparent 2px),
					linear-gradient(rgba(255,255,255,.3) 1px, transparent 1px),
					linear-gradient(90deg, rgba(255,255,255,.3) 1px, transparent 1px);
					background-size: 100px 100px, 100px 100px, 20px 20px, 20px 20px;
					background-position:-2px -2px, -2px -2px, -1px -1px, -1px -1px;
				</code>
				<p><span>Fig e</span><span>Layered Gradient</span></p>
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
	.c-grad {
		min-height: 50vw;
		display: flex;
		flex-direction: column;
		align-items: centre;
	}
	.c-grad--1 {
		background: linear-gradient(180deg, #FFFFFF 0%, #000000 100%), linear-gradient(90deg, #FFFFFF 0%, #000000 100%), #FF0000;
		background-blend-mode: multiply, screen, normal;
	}
	.c-grad--2 {
		background: radial-gradient(65% 100% at 50% 0%, #00FF94 0%, rgba(0, 255, 148, 0.25) 100%), linear-gradient(230deg, #000000 25%, #170059 100%), linear-gradient(215deg, #FFEBB9 10%, #19004E 80%), radial-gradient(100% 245% at 100% 100%, #FFFFFF 0%, #000353 100%), linear-gradient(125deg, #1400FF 0%, #3A0000 100%), linear-gradient(225deg, #00F0FF 30%, #000B6F 45%, #00EBFC 45%, #001676 65%, #00E1F6 65%, #001676 85%, #00ECFD 85%, #001676 100%), linear-gradient(135deg, #00F0FF 0%, #000B6F 15%, #00EBFC 15%, #001676 35%, #00E1F6 35%, #001676 55%, #00ECFD 55%, #001676 100%);
		background-blend-mode: soft-light, screen, overlay, overlay, difference, overlay, normal;
	}
	.c-grad--3 {
		background: radial-gradient(circle at 50% 50%, #FFFFFF 0%, #000000 100%), conic-gradient(red, yellow, lime, aqua, blue, fuchsia, red);
		background-blend-mode: color-dodge, normal;
	}
	.c-grad--4 {
		background:
		linear-gradient(-45deg, white 25%, transparent 25%, transparent 75%, black 75%, black) 0 0,
		linear-gradient(-45deg, black 25%, transparent 25%, transparent 75%, white 75%, white) 1em 1em,
		linear-gradient(45deg, black 17%, transparent 17%, transparent 25%, black 25%, black 36%, transparent 36%, transparent 64%, black 64%, black 75%, transparent 75%, transparent 83%, black 83%) 1em 1em;
		background-color: white;
		background-size: 2em 2em;
	}
	.c-grad--5 {
		background-color:#269;
		background-image: linear-gradient(white 2px, transparent 2px),
		linear-gradient(90deg, white 2px, transparent 2px),
		linear-gradient(rgba(255,255,255,.3) 1px, transparent 1px),
		linear-gradient(90deg, rgba(255,255,255,.3) 1px, transparent 1px);
		background-size: 100px 100px, 100px 100px, 20px 20px, 20px 20px;
		background-position:-2px -2px, -2px -2px, -1px -1px, -1px -1px;
	}

</style>