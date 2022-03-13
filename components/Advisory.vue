<template>
	<section id="advisory_sec">
		<p>Danışma Kurulu</p>
		<div id="advisors_ctn">
			<profile class="advisor_profile" v-for="(advisor, i) in advisors" :key="i" v-bind:profile="advisor" />
		</div>
	</section>
</template>

<script>
import Profile from "./Profile.vue";
export default {
	components: { Profile },
	data() {
		return {
			advisors: [
				{
					img: "../../assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "../../assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "../../assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "../../assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
				{
					img: "../../assets/img/profile.png",
					name: "Ali Yaşar Topçu",
					position: "Farba Otomotiv",
					quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar.",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
#advisory_sec {
	background: #e3e4ff;
	text-align: center;
	margin: 0px 0px 94px 0px;
	p {
		font-style: normal;
		font-weight: 900;
		font-size: 32px;
		line-height: 40px;
		letter-spacing: 0.6px;
		color: #121f3d;
		padding: 55px 0 82px 0;
	}
	#advisors_ctn {
		display: flex;
		flex-flow: row wrap;
		justify-content: center;
		padding-bottom: 86px;
		.advisor_profile {
			color: #121f3d;
			padding: 0 96px;
		}
	}
}
</style>
