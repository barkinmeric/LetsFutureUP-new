<template>
	<section class="index">
		<!-- <li v-for="mountain of test">{{ mountain.name }}</li> -->
		<social-head :title="$t('index.title')" :description="$t('index.desc')" />
		<introduction />
		<hello-career />
		<mentors />
		<newsletter />
		<advisory />
		<partner />
		<subscribe />
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

	data() {
		return {
			test: [],
		};
	},
	// async fetch() {
	// 	this.test = await fetch("https://letsfutureup-api.herokuapp.com/api/data").then((res) => res.json());
	// },
};
</script>

<style lang="scss" scoped></style>
