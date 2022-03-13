<template>
	<div class="hello-career">
		<div class="container">
			<div class="hello-career-title">
				<h1>Let’s FutureUP ile Kariyerine Merhaba De!</h1>
				<p>Let’s FutureUP içerisinde mentorluktan eğitimlere, sektörlerinde bir çok öncü isimle görüşebilme ve tanışma fırsatı yakalayabilirsin.</p>
			</div>
			<div class="grid-container">
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
	padding: 100px 0px 94px 0px;
	background: white;
	.hello-career-title {
		color: $mainColor;
		text-align: center;
		h1 {
			padding: 20px 0px 40px 0px;
			margin: 0;
			font-size: 32px;
			font-weight: 900;
			letter-spacing: 1px;
			line-height: 44px;
		}
		p {
			padding: 0px 0px 100px 0px;
			margin: 0;
			font-size: 20px;
			font-weight: 400;
			letter-spacing: 0.3px;
			line-height: 34px;
		}
		.green {
			color: $sideColor;
		}
	}
	.grid-container {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(392px, 1fr));
		column-gap: 52px;
		justify-content: center;
		text-align: center;
	}
}
</style>
