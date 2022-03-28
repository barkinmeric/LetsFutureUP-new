<template>
	<div class="hello-career">
		<div class="container">
			<h1 class="hello-career-title">Let’s FutureUP ile Kariyerine Merhaba De!</h1>
			<p class="hello-career-text">
				Let’s FutureUP içerisinde mentorluktan eğitimlere, sektörlerinde bir çok <br />
				öncü isimle görüşebilme ve tanışma fırsatı yakalayabilirsin.
			</p>
			<div class="hello-career-body">
				<hello-career-card />
				<hello-career-card />
				<hello-career-card />
				<hello-career-card />
				<hello-career-card />
				<hello-career-card />
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
	padding: 0px 0px 28px 0px;
	background: $backgroundColor;
	.hello-career-title {
		color: $titleColor;
		text-align: center;
		padding: 0px 0px 40px 0px;
		margin: 0;
		font-size: 32px;
		font-weight: 900;
		letter-spacing: 1px;
		line-height: 44px;
	}
	.hello-career-text {
		color: $textColor;
		text-align: center;
		padding: 0px 0px 100px 0px;
		margin: 0;
		font-size: 20px;
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
