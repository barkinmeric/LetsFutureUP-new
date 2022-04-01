<template>
	<section id="mentors_sec">
		<div id="title_ctn">
			<p>Kariyerinin Zirvesindeki İsimlerden Let’s FutureUP</p>
			<div></div>
		</div>
		<div id="mentors_ctn">
			<VueSlickCarousel :dots="true" v-bind="settings">
				<mentor-card v-for="(mentor, i) in mentors" :key="i" v-bind:mentor="mentor" />
			</VueSlickCarousel>
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
			mentors: [
				{
					img: "@/assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "@/assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "@/assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "@/assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
			],
			settings: {
				arrows: false,
				dots: true,
				focusOnSelect: true,
				infinite: true,
				speed: 500,
				slidesToShow: 3,
				slidesToScroll: 3,
				touchThreshold: 5,
				responsive: [
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
#mentors_sec {
	box-sizing: border-box;
	background: #ecf4fc;
	#title_ctn {
		padding: 40px 10vw 20px 10vw;
		@media (max-width: $mobile_bp) {
			padding-top: 0px;
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
				font-size: 1.5rem;
				width: inherit;
			}
		}
	}
	#mentors_ctn {
		margin: 0 1.6vw;
		padding: 70px 0;
	}
}
</style>
