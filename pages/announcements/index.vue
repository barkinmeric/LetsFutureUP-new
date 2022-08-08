<template>
	<div>
		<social-head :title="$t('announcements.title')" :description="$t('index.desc')" />
		<div>
			<h1 class="container">{{ $t("announcements.title") }}</h1>
		</div>
		<announcements-list-ctn></announcements-list-ctn>
	</div>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("announcements.title")} ${this.$i18n.t("url")}`,
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
