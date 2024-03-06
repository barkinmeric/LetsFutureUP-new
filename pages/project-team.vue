<template>
	<section class="project-team">
		<social-head :title="$t('team.title')" :description="$t('team.desc')" />
		<div class="container">
			<dep-selection-bar @scroll-to-sec="ScrollToSec" />
			<dep-sections v-for="(secData, i) in $t('team.teams')" :key="i" :secData="secData" />
		</div>
	</section>
</template>
<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${$t("team.title")} ${$t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: $t("team.desc"),
				},
			],
		};
	},
	methods: {
		ScrollToSec(id) {
			document.getElementById(id).scrollIntoView();
		},
	},
};
</script>

<style lang="scss" scope></style>
