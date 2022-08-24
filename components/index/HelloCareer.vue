<template>
	<div class="hello-career">
		<div class="container">
			<h2 class="hello-career-title">{{ $t("index.hello-career.title") }}</h2>
			<p v-html="$t('index.hello-career.desc')" class="hello-career-text"></p>
			<div class="hello-career-body">
				<hello-career-card v-for="(item, index) in $t('index.hello-career.content')" :key="item.title" :item="item" :index="index" />
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "HelloCareer",
};
</script>

<style lang="scss" scoped>
.hello-career {
	padding: 0 5px 50px 5px;
	background: $backgroundColor;
	.hello-career-title {
		color: $titleColor;
		text-align: center;
		padding: 0px 0px 40px 0px;
		margin: 0;
		font-size: 28px;
		font-weight: 900;
		letter-spacing: 1px;
		line-height: 44px;
	}
	.hello-career-text {
		color: $textColor;
		text-align: center;
		padding: 0px 0px 100px 0px;
		margin: 0;
		font-size: 1.25rem;
		font-weight: 400;
		letter-spacing: 0.3px;
		line-height: 34px;
	}
	.hello-career-body {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(392px, 1fr));
		column-gap: 52px;
		justify-content: center;
		text-align: center;
	}
}
</style>
