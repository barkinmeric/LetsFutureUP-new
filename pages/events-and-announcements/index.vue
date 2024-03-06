<template>
	<section class="events-announcements" v-if="false">
		<social-head :title="$t('events-announcements.title')" :description="$t('index.desc')" />
		<div class="container">
			<h1>{{ $t("events-announcements.title") }}</h1>
			<main-item-ctn :item="$t('events-announcements.content')[0]"></main-item-ctn>
			<h2>Daha Fazla</h2>
			<ul class="events-list">
				<item-ctn v-for="(item, i) in $t('events-announcements.content').slice(1)" :key="i" :item="item"></item-ctn>
			</ul>
		</div>
	</section>
</template>
<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${$t("events-announcements.title")} ${$t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: $t("index.desc"),
				},
			],
		};
	},
		beforeCreate() {
		router.push('/' + $locale)
	},
};
</script>

<style lang="scss" scoped>
.events-announcements {
	display: flex;
	flex-flow: column nowrap;
	h2 {
		margin: 70px 0 0 0;
	}
	.events-list {
		display: flex;
		flex-flow: row wrap;
		justify-content: space-between;
	}
}
</style>
