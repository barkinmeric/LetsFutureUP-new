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
	margin: 0 auto 66px auto;
	.card-item {
		display: grid;
		grid-template-columns: 100%;
		justify-content: center;
		background: white;
		border-radius: 10px;
		.card-head {
			height: 260px;
			width: 392px;
			img {
				user-select: none;
				border-radius: 16px;
			}
		}
		.card-body {
			display: grid;
			grid-template-columns: 100%;
			text-align: center;
			justify-content: center;
			h5 {
				display: inline-block;
				font-size: 1.125rem;
				font-weight: 900;
				letter-spacing: 0.3px;
				line-height: 28px;
				color: $titleColor;
				padding: 16px 0px 8px 0px;
			}
			p {
				font-size: .875rem;
				font-weight: 400;
				letter-spacing: 0.3px;
				line-height: 24px;
				color: $textColor;
			}
		}
	}
}
</style>
