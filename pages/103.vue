<template>
	<main>
		<div class="c-text-container">
			<h1>Stepped Gradients</h1>
			<h2>103</h2>
		</div>
		<div class="c-grad__wrapper">
			<div class="c-grad-container">
				<div class="c-grad c-grad--linear">
					</div>
				<code>
					background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(255,255,255,1) 100%);
				</code>
				<p><span>Fig b</span><span>Stepped Gradient</span></p>
			</div>
			<div class="c-grad-container">
				<div class="c-grad c-grad--scrim">
					</div>
				<code>
					@include scrimGradient(black);
				</code>
				<p><span>Fig a</span><span>Linear Gradient</span></p>
			</div>
		</div>
	</main>
</template>

<style scoped lang="scss">
	main {

	}
	@mixin scrimGradient($startColor: black, $direction: 'to bottom', $ease: 'ease-in-out', $offsetStart: 0, $offsetEnd: 100) {
	  
	  // ease out
	  $scrimCoordinatesEaseOut: (
	    0: 1,
	    19: 0.738,
	    34: 0.541,
	    47: 0.382,
	    56.5: 0.278,
	    65: 0.194,
	    73: 0.126,
	    80.2: 0.075,
	    86.1: 0.042,
	    91: 0.021,
	    95.2: 0.008,
	    98.2: 0.002,
	    100: 0
	  );
	  
	  // ease in out
	  $scrimCoordinatesEaseInOutSine: (
	    0: 1,
	    9.5: 0.978,
	    17.7: 0.925,
	    24.7: 0.857,
	    31: 0.781,
	    36.8: 0.701,
	    42.3: 0.62,
	    47.6: 0.538,
	    52.9: 0.455,
	    58.2: 0.373,
	    63.7: 0.291,
	    69.5: 0.212,
	    75.8: 0.138,
	    82.9: 0.07,
	    91.2: 0.019,
	    100: 0
	  );
	  
	  $hue: hue($startColor);
	  $saturation: saturation($startColor);
	  $lightness: lightness($startColor);
	  $stops: ();
	  $scrimCoordinates: $scrimCoordinatesEaseOut;
	  
	  @if $ease == 'ease-in-out-sine' {
	    $scrimCoordinates: $scrimCoordinatesEaseInOutSine;
	  } 
	  
	  @each $colorStop, $alphaValue in $scrimCoordinates {
	    $stop: hsla($hue, $saturation, $lightness, $alphaValue) percentage((($offsetEnd - $offsetStart) * $colorStop/100 + $offsetStart)/100);
	    $stops: append($stops, $stop, comma);
	  }
	  
	  background: linear-gradient(unquote($direction), $stops);
	  
	}

	.c-text-container {
		text-align: center;
	}
	.c-grad__wrapper {
		display: grid;
		grid-template-columns: repeat(12, [col-start] 1fr);
		padding: 3vw;
	}
	.c-grad-container {
		grid-column: auto / span 6;
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
		&--scrim {
			position: relative;
			&::before {
				content: '';
				top: 0;
				left: 0;
				right: 0;
				bottom: 0;
				width: 100%;
				height: 25vw;
				@include scrimGradient(black);
			}
		}
		&--linear {
			background: linear-gradient(rgba(0,0,0,1) 0%, rgba(255,255,255,1) 50%);
		}
	}
</style>