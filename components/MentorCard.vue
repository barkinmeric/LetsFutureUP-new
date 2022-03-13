<template>
	<div id="mentor_card">
		<profile class="mentor_profile" v-bind:profile="{ img: mentor.img, name: mentor.name, position: mentor.position }" />
		<div id="quote_ctn">
			<p>{{ mentor.quote }}</p>
		</div>
	</div>
</template>

<script>
import Profile from "./Profile.vue";
export default {
	components: { Profile },
	props: ["mentor"],
};
</script>

<style lang="scss" scoped>
#mentor_card {
	width: 300px;
	height: 436px;
	text-align: center;
	background: #121f3d;
	box-shadow: 0px 4px 30px rgba(0, 0, 0, 0.05);
	border-radius: 16px;
	padding: 32px;
	margin: 9px 9px 0px 9px;
	.mentor_profile {
		color: white;
	}
	#quote_ctn {
		padding-top: 23px;
		font-style: normal;
		font-weight: normal;
		font-size: 14px;
		line-height: 24px;
		letter-spacing: 0.3px;
		color: #d0d2d8;
	}
}
</style>
