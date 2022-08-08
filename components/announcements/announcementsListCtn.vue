<template>
	<section class="container events-main">
		<main-announcement-ctn :item="$t('announcements.content').reverse()[0]"></main-announcement-ctn>
		<h2>Daha Fazla</h2>
		<ul class="events-list">
			<announcement-ctn
				v-for="(announcement, i) in $t('announcements.content').reverse().slice(1)"
				:key="i"
				:item="announcement"
			></announcement-ctn>
		</ul>
	</section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.events-main {
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
