<template>
	<section class="mentorship-program">
		<social-head :title="$t('mentorship.title')" :description="$t('index.desc')" />
		<div class="container">
			<mentor-section />
			<ment-grid :mentGrid="mentorGridData" />
			<mentee-section />
			<ment-grid :mentGrid="menteeGridData" />
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
		}
	},
	beforeCreate() {
		this.$router.push('/' + this.$i18n.locale)
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
