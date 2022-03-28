<template>
	<div class="partner">
		<div class="container">
			<div class="partner-part">
				<div class="partner-title">{{ $t("index.partner.title") }}</div>
				<div class="flex-container">
					<partner-modal v-for="image in $t('index.partner.content')" :key="image" :image="image" />
				</div>
			</div>
			<div class="partner-part">
				<div class="partner-title">{{ $t("index.supporter.title") }}</div>
				<div class="flex-container">
					<partner-modal v-for="image in $t('index.supporter.content')" :key="image" :image="image" />
				</div>
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
	background: $backgroundColor;
	padding: 0px 0 120px 0;
	.partner-part {
		.partner-title {
			text-align: center;
			color: $titleColor;
			padding: 0px 0px 32px 0px;
			font-size: 32px;
			font-weight: 900;
			letter-spacing: 0.6px;
			line-height: 40px;
		}
		.flex-container {
			padding: 0 0 64px 0;
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
			gap: 40px;
		}
	}
}
</style>
