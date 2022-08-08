<template>
	<div>
		<social-head :title="$t('events.title')" :description="$t('index.desc')" />
		<div>
			<h1 class="container">{{ $t("events.title") }}</h1>
		</div>
		<events-list-ctn></events-list-ctn>
	</div>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("events.title")} ${this.$i18n.t("url")}`,
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

<style></style>
