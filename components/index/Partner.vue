<template>
	<div id="partner">
		<div class="container">
			<div class="partner-part">
				<div class="partner-title">{{ $t("index.partner.title") }}</div>
				<div class="flex-container">
					<partner-modal v-for="(image, i) in $t('index.partner.content')" :key="i" :link="image.link" :image="image.img" />
				</div>
			</div>
			<div class="partner-part">
				<div class="partner-title">{{ $t("index.supporter.title") }}</div>
				<div class="flex-container">
					<partner-modal v-for="(image, i) in $t('index.supporter.content')" :key="i" :link="image.link" :image="image.img" />
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
#partner {
	background: $backgroundColor;
	padding: 20px 10px;
	margin-bottom: 80px;
	.partner-part {
		.partner-title {
			text-align: center;
			color: $titleColor;
			padding: 40px 10px 20px 10px;
			font-size: 28px;
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
