<template>
	<div class="advisor">
		<div class="img_ctn">
			<nuxt-img
				class="image"
				format="jpg"
				height="167px"
				width="167px"
				:alt="advisor.name"
				draggable="false"
				loading="lazy"
				:src="advisor.image"
			/>
		</div>
		<div class="info_ctn">
			<p class="profile_name">{{ advisor.name }}</p>
			<p class="profile_place">{{ advisor.place }}</p>
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
		.image {
			background-size: cover;
			border-radius: 50%;
			margin: auto;
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
		.profile_place {
			padding-top: 6px;
			font-size: 18px;
			font-weight: 600;
		}
		.profile_pos {
			padding-top: 6px;
			font-size: 16px;
			font-weight: 400;
		}
	}
}
</style>
