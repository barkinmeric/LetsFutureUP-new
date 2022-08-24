<template>
	<section id="mentors-wrp">
		<div id="mentors_sec" class="container">
			<div id="title_ctn">
				<p>Kariyerinin Zirvesindeki İsimlerden Let’s FutureUP</p>
				<div></div>
			</div>
			<div id="mentors_ctn">
				<VueSlickCarousel :dots="true" v-bind="settings">
					<mentor-card v-for="(mentor, i) in $t('index.opinion.content')" :key="i" v-bind:mentor="mentor" />
				</VueSlickCarousel>
			</div>
		</div>
	</section>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
export default {
	components: { VueSlickCarousel },
	data() {
		return {
			settings: {
				arrows: false,
				dots: true,
				focusOnSelect: false,
				infinite: true,
				speed: 500,
				slidesToShow: 4,
				slidesToScroll: 3,
				touchThreshold: 5,
				responsive: [
					{
						breakpoint: 1400,
						settings: {
							slidesToShow: 3,
							slidesToScroll: 2,
							infinite: true,
							dots: true,
						},
					},
					{
						breakpoint: 1200,
						settings: {
							slidesToShow: 2,
							slidesToScroll: 2,
							infinite: true,
							dots: true,
						},
					},
					{
						breakpoint: 600,
						settings: {
							slidesToShow: 1,
							slidesToScroll: 1,
							infinite: true,
							dots: true,
						},
					},
				],
			},
		};
	},
};
</script>

<style lang="scss" scoped>
$tablet_bp: 1200px;
$mobile_bp: 600px;
#mentors-wrp {
	background: #ecf4fc;
	#mentors_sec {
		box-sizing: border-box;
		margin-bottom: 100px;
		#title_ctn {
			padding: 40px 0vw 20px 0vw;
			@media (max-width: $mobile_bp) {
				padding-top: 40px;
				font-size: 50%;
			}
			p {
				font-style: normal;
				font-weight: 900;
				font-size: 2rem;
				line-height: 44px;
				letter-spacing: 0.6px;
				width: 650px;
				color: #121f3d;
				@media (max-width: $tablet_bp) {
					text-align: center;
					width: inherit;
				}
				margin: auto;
				text-align: center;
			}
		}
		#mentors_ctn {
			margin: 0 0;
			padding: 70px 0;
		}
	}
}
</style>
