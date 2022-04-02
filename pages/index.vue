<template>
	<section class="index">
		<social-head :title="$t('index.title')" :description="$t('index.desc')" />
		<introduction />
		<hello-career />
		<mentors />
		<newsletter />
		<advisory />
		<partner />
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("index.title")} ${this.$i18n.t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: this.$i18n.t("index.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped></style>
