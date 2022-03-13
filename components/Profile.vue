<template>
	<div class="profile">
		<div class="img_ctn">
			<!-- <img :src="profile.img"> -->
			<img src="@/assets/img/profile.png" />
		</div>
		<div class="info_ctn">
			<p class="profile_name">{{ profile.name }}</p>
			<p class="profile_pos">{{ profile.position }}</p>
		</div>
	</div>
</template>

<script>
export default {
	props: ["profile"],
};
</script>

<style lang="scss">
.profile {
	.img_ctn {
		img {
			border-radius: 50%;
		}
	}
	.info_ctn {
		padding-top: 25px;
		font-style: normal;
		font-weight: normal;
		font-size: 18px;
		line-height: 23px;

		text-align: center;
		letter-spacing: 0.6px;
		// color: white;

		.profile_name {
			font-weight: 900;
		}
		.profile_pos {
			padding-top: 6px;
		}
	}
}
</style>
