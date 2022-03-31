<template>
	<section id="advisory_sec">
		<p>Danışma Kurulu</p>
		<VueSlickCarousel :dots="true" v-bind="settings">
			<advisor class="advisor_profile" v-for="(advisor, i) in advisors" :key="i" v-bind:advisor="advisor" />
		</VueSlickCarousel>
	</section>
</template>

<script>
import Advisor from "./Advisor.vue";
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
export default {
	components: { Advisor, VueSlickCarousel },
	data() {
		return {
			advisors: [
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
	methods: {
		swipeLeft() {},
		swipeRight() {},
	},
};
</script>

<style lang="scss" scoped>
$tablet_bp: 1200px;
$mobile_bp: 600px;
#advisory_sec {
	background: #ecf4fc;
	text-align: center;
	padding-bottom: 90px;
	p {
		font-style: normal;
		font-weight: 900;
		font-size: 32px;
		line-height: 40px;
		letter-spacing: 0.6px;
		color: #121f3d;
		padding: 55px 0 82px 0;
	}
}
</style>
