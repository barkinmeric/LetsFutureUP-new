<template>
	<section class="mentorship-program">
		<social-head :title="$t('mentorship.title')" :description="$t('index.desc')" />
		<div class="container">
			<mentor-section />
			<ment-grid :mentGrid="$t('mentorship.years.2021-2022.mentors')" />
			<mentee-section />
			<ment-grid :mentGrid="$t('mentorship.years.2021-2022.mentees')" />
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("mentorship.title")} ${this.$i18n.t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: this.$i18n.t("mentorship.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scope></style>
