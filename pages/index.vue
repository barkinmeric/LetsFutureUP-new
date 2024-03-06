<template>
	<section class="index">
		<social-head :title="$t('index.title')" :description="$t('index.desc')" />
		<introduction />
		<hello-career />
		<mentors />
		<!-- <newsletter /> -->
		<advisory />
		<partner />
		<!-- <subscribe /> -->
		<join-us />
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${$t("index.title")} ${$t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: $t("index.desc"),
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
