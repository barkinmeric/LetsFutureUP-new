<template>
	<div class="advisor">
		<div class="img_ctn">
			<img />
		</div>
		<div class="info_ctn">
			<p class="profile_name">{{ advisor.name }}</p>
			<p class="profile_pos">{{ advisor.position }}</p>
		</div>
	</div>
</template>

<script>
export default {
	props: ["advisor"],
};
</script>

<style lang="scss" scoped>
.advisor {
	padding: 47px;
	.img_ctn {
		width: 170px;
		height: 170px;
		background: url("/pages/index/advisorProfile.png") no-repeat center;
		background-size: cover;
		border-radius: 50%;
		margin: auto;
	}
	.info_ctn {
		padding-top: 25px;
		font-style: normal;
		font-weight: normal;
		font-size: 1.125rem;
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
