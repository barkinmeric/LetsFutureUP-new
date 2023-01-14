<template>
	<section class="ments-sec">
		<h2>{{ mentGrid.title }}</h2>
		<div class="flex-container">
			<div class="ment-ctn" v-for="(ment, i) in mentGrid.content" :key="i">
				<nuxt-img format="jpg" class="ment-img" draggable="false" :src="ment.image" :alt="ment.name" height="260" width="287" />
				<p class="ment-name">{{ ment.name }}</p>
				<p>{{ ment.place }}</p>
				<p v-if="isMentor">{{ ment.position }}</p>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	props: {
		mentGrid: Object,
		isMentor: Boolean,
	},
};
</script>

<style lang="scss" scope>
.ments-sec {
	text-align: center;
	padding: 48px 14px 64px 14px;
	background: #f3f4f5;
	border-radius: 8px;
	.flex-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		.ment-ctn {
			margin-top: 38px;
			width: 307px;
			.ment-img {
				border-radius: 8px;
				margin: 10px;
			}
			.ment-name {
				font-style: normal;
				font-weight: 900;
				font-size: 18px;
				line-height: 23px;
				text-align: center;
			}
		}
	}
}
</style>
