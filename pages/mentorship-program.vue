<template>
	<section class="mentorship-program">
		<social-head :title="$t('mentorship.title')" :description="$t('index.desc')" />
		<div class="container">
			<mentor-section />
			<ment-grid :mentGrid="$t('mentorship.years.2021-2022.mentors')" :isMentor="true"/>
			<mentee-section />
			<ment-grid :mentGrid="$t('mentorship.years.2021-2022.mentees')" :isMentor="false"/>
			<div class="center">
				<h1 class="mentorship-header">{{ $t("mentorship.years.2020-2021.title") }}</h1>
			</div>
			<ment-grid :mentGrid="$t('mentorship.years.2020-2021.mentors')" :isMentor="true"/>
			<ment-grid :mentGrid="$t('mentorship.years.2020-2021.mentees')" :isMentor="false"/>
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

<style lang="scss" scope>
.mentorship-program {
	.center {
		text-align: center;
		padding-top: 50px;
	}
}
</style>
