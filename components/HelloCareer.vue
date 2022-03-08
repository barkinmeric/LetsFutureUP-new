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
	padding: 20px 0px 10px 0px;
	background: white;
	.hello-career-title {
		padding: 10px 0px 20px 0px;
		color: $mainColor;
		text-align: center;
		h1 {
			margin: 0;
			font-size: 26px;
			font-weight: 600;
		}
		p {
			margin: 0;
			font-size: 20px;
			font-weight: 400;
		}
		.green {
			color: $sideColor;
		}
	}
	.grid-container {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(392px, 1fr));
		column-gap: 10px;
		justify-content: center;
		text-align: center;
	}
}
</style>
