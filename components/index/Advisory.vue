<template>
	<section id="adv-wrp">
		<section id="advisory_sec" class="container">
			<p>Danışma Kurulu</p>
			<VueSlickCarousel :dots="true" v-bind="settings">
				<advisor class="advisor_profile" v-for="(advisor, i) in $t('index.board.content')" :key="i" v-bind:advisor="advisor" />
			</VueSlickCarousel>
		</section>
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
			advisors: [
				{
					img: "/pages/index/advisorProfile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "/pages/index/advisorProfile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "/pages/index/advisorProfile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "/pages/index/advisorProfile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "/pages/index/advisorProfile.png",
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
				slidesToShow: 5,
				slidesToScroll: 3,
				touchThreshold: 5,
				responsive: [
					{
						breakpoint: 1400,
						settings: {
							slidesToShow: 4,
							slidesToScroll: 2,
							infinite: true,
							dots: true,
						},
					},
					{
						breakpoint: 1200,
						settings: {
							slidesToShow: 3,
							slidesToScroll: 2,
							infinite: true,
							dots: true,
						},
					},
					{
						breakpoint: 800,
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
	methods: {
		swipeLeft() {},
		swipeRight() {},
	},
};
</script>

<style lang="scss" scoped>
$tablet_bp: 1200px;
$mobile_bp: 600px;
	#adv-wrp {
		background: #ecf4fc;
		#advisory_sec {
			text-align: center;
			padding-bottom: 90px;
			p {
				font-style: normal;
				font-weight: 900;
				font-size: 2rem;
				line-height: 40px;
				letter-spacing: 0.6px;
				color: #121f3d;
				padding: 55px 0 82px 0;
			}
		}
	}
</style>
