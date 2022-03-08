<template>
	<div class="hello-career-card">
		<div class="card-item">
			<div class="card-head">
				<nuxt-img format="jpg" src="/pages/index/slider/desktop/en/1.webp" height="260px" width="392px" alt="StartUP" draggable="false" loading="lazy" />
			</div>
			<div class="card-body">
				<NuxtLink to="/"><h5>StartUP</h5> </NuxtLink>
				<p>Geleceğine emin adımlarla ilerleyen, yaratıcı ve başarılı gençleri desteklemek amacıyla ortaya çıkmıştır. Geleceğin başarılı isimlerinin pek çok alanda kendini geliştirmiş,</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "HelloCareerCard",
};
</script>

<style lang="scss" scoped>
.hello-career-card {
	height: 400px;
	width: 392px;
	margin: 0 auto;
	.card-item {
		display: grid;
		grid-template-columns: 100%;
		justify-content: center;
		background: white;
		border-radius: 10px;
		.card-head {
			height: 260px;
			width: 392px;
			margin: 0;
			padding: 0;
			img {
				user-select: none;
				border-radius: 10px;
			}
		}
		.card-body {
			padding: 0px;
			display: grid;
			grid-template-columns: 100%;
			text-align: center;
			justify-content: center;
			h5 {
				display: inline-block;
				font-size: 18px;
				font-weight: 1000;
				letter-spacing: 0.3px;
				padding: 5px 0px;
				color: $mainColor;
				text-transform: uppercase;
				border-bottom: 1px solid $sideColor;
				border-bottom-width: 3px;
				padding-bottom: 3px;
			}
			p {
				margin: 10px 0px;
				font-size: 14px;
				font-weight: 400;
				color: $mainColor;
			}
		}
	}
}
</style>
