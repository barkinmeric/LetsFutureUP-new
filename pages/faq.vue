<template>
	<section class="faq">
		<social-head :title="$t('faq.title')" :description="$t('faq.desc')" />
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
					content: this.$i18n.t("faq.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scope>
.faq {
	margin-top: 32px;
	margin-bottom: 30px;
}
</style>
