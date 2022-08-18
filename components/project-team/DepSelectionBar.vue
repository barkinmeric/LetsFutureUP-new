<template>
	<nav id="barNav">
		<VueSlickCarousel id="navCarousel" v-bind="settings">
			<button @click="ScrollToSec('humanRsr')" class="btn">İnsan Kaynakları Departmanı</button>
			<button @click="ScrollToSec('corCom')" class="btn">Kurumsal İletişim Departmanı</button>
			<button @click="ScrollToSec('busStr')" class="btn">İş & Strateji Geliştirme Departmanı</button>
			<button @click="ScrollToSec('forAf')" class="btn">Dış İlişkiler Departmanı</button>
			<button @click="ScrollToSec('socMed')" class="btn">Sosyal Medya ve Dijital Pazarlama Departmanı</button>
			<button @click="ScrollToSec('startUp')" class="btn">Startup Departmanı</button>
		</VueSlickCarousel>
	</nav>
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
				dots: false,
				focusOnSelect: true,
				infinite: false,
				speed: 500,
				slidesToShow: 6,
				slidesToScroll: 3,
				touchThreshold: 5,
				responsive: [
					{
						breakpoint: 1200,
						settings: {
							slidesToShow: 4,
							slidesToScroll: 2,
							infinite: false,
							dots: false,
						},
					},
					{
						breakpoint: 600,
						settings: {
							slidesToShow: 2,
							slidesToScroll: 3,
							infinite: false,
							dots: false,
						},
					},
				],
			},
		};
	},
	methods: {
		ScrollToSec(id) {
			this.$emit("scroll-to-sec", id);
		},
	},
};
</script>

<style lang="scss" scoped>
#barNav {
	display: static;
	height: 80px;
	background: $depNav_background;
	border-radius: 8px;
	padding: 4px;
	margin-bottom: 114px;
	.btn {
		width: 200px;
		height: 72px;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		padding: 12px 8px;
		font-style: normal;
		font-weight: 400;
		font-size: 16px;
		line-height: 24px;
		text-align: center;
		letter-spacing: 0.3px;
		border-radius: 8px;
		background: $depNav_background;
		&:focus {
			background: $sideColor;
			border-radius: 8px;
			color: $backgroundColor;
		}
		&:hover {
			background: #d0d0d7;
		}
	}
}
</style>
