<template>
	<div class="partner">
		<div class="container">
			<div class="partner-title">{{ $t("index.partner.title") }}</div>
			<div class="flex-container">
				<partner-modal v-for="image in $t('index.partner.content')" :key="image" :image="image" />
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "Partner",
};
</script>

<style lang="scss" scoped>
.partner {
	background: white;
	color: $mainColor;
	padding-bottom: 20px;
	.partner-title {
		text-align: center;
		padding: 20px 0px 10px 0px;
		font-size: 22px;
		font-weight: 600;
	}
	.flex-container {
		padding-top: 10px;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 40px;
	}
}
</style>
