<template>
	<section class="faq">
		<social-head :title="$t('faq.title')" :description="$t('index.desc')" />
		<div class="container">
			<div v-for="item in $t('faq.content')" :key="item.title">
				<faq-collapsible :title="item.title" :text="item.text" />
			</div>
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("faq.title")} ${this.$i18n.t("url")}`,
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

<style lang="scss" scope>
.faq {
	margin-top: 133px;
	margin-bottom: 229px;
}
</style>
