<template>
	<div class="partner-modal">
		<nuxt-img format="jpg" :src="image" alt="partner" width="392px" height="100px" draggable="false" loading="lazy" />
	</div>
</template>

<script>
export default {
	name: "PartnerModal",
	props: {
		image: String,
	},
};
</script>

<style lang="scss" scoped>
.partner-modal {
	border: 1px solid;
	border-radius: 8px;
	border-color: $thirdColor;
	img {
		user-select: none;
		padding: 30px 133px;
		filter: grayscale(100%);
	}
}
</style>
