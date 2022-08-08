<template>
	<section class="container events-main">
		<main-event-ctn :item="$t('events.content')[0]"></main-event-ctn>
		<h2>Daha Fazla</h2>
		<ul class="events-list">
			<event-ctn v-for="(event, i) in $t('events.content').slice(1).reverse()" :key="i" :item="event"></event-ctn>
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
