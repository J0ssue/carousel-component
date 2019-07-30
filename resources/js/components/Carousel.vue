<template>
	<div>
		<slot></slot>
	</div>
</template>

<script>
	import Flickity from "flickity";
	import "flickity/dist/flickity.min.css";

	export default {
		props: {
			contain: { default: true },
			cellAlign: { default: "left" },
			wrapAround: { default: true },
			groupCells: { defjault: false },
			autoPlay: { default: false },
			fullscreen: { default: false }
		},

		mounted() {
			new Flickity(this.$el, {
				contain: this.contain,
				cellAlign: this.cellAlign,
				wrapAround: this.wrapAround,
				groupCells: this.groupCells,
				autoPlay: this.autoPlay,
				fullscreen: this.fullscreen
			});
		},

		name: "Carousel"
	};
</script>
