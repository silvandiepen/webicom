<template>
	<div class="logo" :class="[loaded ? 'loaded' : '']">
		<svg
			id="Layer_1"
			version="1.1"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
			x="0px"
			y="0px"
			viewBox="0 0 645.76 252.14"
			style="enable-background:new 0 0 645.76 252.14;"
			xml:space="preserve"
		>
			<g>
				<path class="yellow" d="M396.46,49.67L295.38,201.3H158.86c-6.46,0-10.31-7.2-6.73-12.57l92.7-139.06H396.46z" />
				<polygon class="yellow-shadow" points="244.83,49.67 219.56,87.58 295.38,201.3 " />
			</g>
			<g>
				<polygon class="purple" points="244.83,49.67 345.92,201.3 497.55,201.3 396.46,49.67 " />
				<polygon class="purple-shadow" points="396.46,49.67 345.92,201.3 421.73,87.58 " />
			</g>
			<g>
				<path
					class="red"
					d="M590.25,62.24l-90.3,135.45c-1.5,2.25-4.02,3.6-6.73,3.6h-147.3L444.6,53.27c1.5-2.25,4.02-3.6,6.73-3.6h132.19
	C589.98,49.67,593.83,56.87,590.25,62.24z"
				/>
			</g>
			<g>
				<path
					class="purple"
					d="M51.04,62.24l90.3,135.45c1.5,2.25,4.02,3.6,6.73,3.6h147.3L196.69,53.27c-1.5-2.25-4.02-3.6-6.73-3.6H57.77
	C51.31,49.67,47.46,56.87,51.04,62.24z"
				/>
			</g>
		</svg>
	</div>
</template>
<script>
export default {
	data() {
		return {
			loaded: false
		};
	},
	mounted() {
		const _this = this;
		setTimeout(() => {
			_this.loaded = true;
		}, 500);
	}
};
</script>

<style lang="scss">
@import '~tools';
svg {
	width: grid(6);
	@media #{$small-only} {
		width: grid(12);
	}
}
.yellow {
	fill: #ffcd62;
}
.purple {
	fill: #742a88;
}
.purple-shadow {
	fill: #542163;
}
.red {
	fill: #ee1f50;
}
.purple-shadow {
	fill: #390e43;
}
.yellow-shadow {
	fill: #f99d32;
}
.st7 {
	fill: #ffffff;
}
g {
	transform: scale(0);
	transition: transform 0.3s;

	.loaded & {
		@for $i from 1 through 20 {
			&:nth-child(#{$i}) {
				transform: scale(1);
				transition-delay: #{($i * 0.1)}s;
			}
		}
	}
}
</style>
