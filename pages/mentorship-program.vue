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

	data() {
		return {
			mentorGridData: {
				title: "MENTORLARIMIZ",
				elems: [
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
				],
			},
			menteeGridData: {
				title: "MENTEELERİMİZ",
				elems: [
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
					{
						imgSrc: "/pages/mentorship-program/mentPlaceholder.png",
					},
				],
			},
		};
	},
};
</script>

<style lang="scss" scope></style>
