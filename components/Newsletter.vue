<template>
	<div class="newsletter">
		<div class="container">
			<h1 class="newsletter-title">Duyurular & Etkinlikler</h1>
			<div class="newsletter-body">
				<div class="left-part">
					<nuxt-img format="jpg" src="/pages/index/slider/desktop/en/1.webp" height="392px" width="500px" alt="StartUP" draggable="false" loading="lazy" />
				</div>
				<div class="right-part">
					<div class="right-card">
						<nuxt-img format="jpg" src="/pages/index/slider/desktop/en/1.webp" height="176px" width="176px" alt="StartUP" draggable="false" loading="lazy" />
						<div class="card-desc">
							<h2 class="card-title">EN İYİ KENDİN OL</h2>
							<p class="card-text">
								Let's FutureUP ekibimizin WeTALK etkinlikleri hız kesmeden devam ediyor! Şimdi sırada Anadolu Efes Spor Kulübü Basketbol Oyuncusu Doğuş Balbay var! Sayın Balbay’ın “Potansiyelimin Zirvesine Nasıl Ulaşırım?” konulu
								değerli tecrübelerini paylaşacağı...
							</p>
							<span class="card-tag">Etkinlikler</span>
						</div>
					</div>
					<div class="right-card">
						<nuxt-img format="jpg" src="/pages/index/slider/desktop/en/1.webp" height="176px" width="176px" alt="StartUP" draggable="false" loading="lazy" />
						<div class="card-desc">
							<h2 class="card-title">LET'S FUTUREUP 1. YILINI KUTLUYOR!</h2>
							<p class="card-text">
								Let's FutureUP ekibimizin WeTALK etkinlikleri hız kesmeden devam ediyor! Şimdi sırada Anadolu Efes Spor Kulübü Basketbol Oyuncusu Doğuş Balbay var! Sayın Balbay’ın “Potansiyelimin Zirvesine Nasıl Ulaşırım?” konulu
								değerli tecrübelerini paylaşacağı...
							</p>
							<span class="card-tag">Duyurular</span>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "Newsletter",
};
</script>

<style lang="scss" scoped>
.newsletter {
	padding: 69px 0px 89px 0px;
	background: white;
	.newsletter-title {
		color: $mainColor;
		padding: 0px 0px 36px 0px;
		font-size: 32px;
		font-weight: 900;
		letter-spacing: 0.6px;
		line-height: 40px;
	}
	.newsletter-body {
		display: flex;
		gap: 40px;
		img {
			user-select: none;
			border-radius: 8px;
		}
		.left-part {
			height: 392px;
		}
		.right-part {
			max-width: 650px;
			display: grid;
			grid-template-columns: 100%;
			row-gap: 40px;
			.right-card {
				height: 176px;
				display: flex;
				gap: 16px;
				.card-desc {
					display: grid;
					grid-template-columns: 100%;
					.card-title {
						font-size: 18px;
						font-weight: 900;
						letter-spacing: 0.6px;
						line-height: 34px;
					}
					.card-text {
						font-size: 14px;
						font-weight: 400;
						letter-spacing: 0.6px;
						line-height: 20px;
					}
					.card-tag {
						height: 32px;
						width: 97px;
						padding: 6px 16px;
						text-align: center;
						font-size: 14px;
						font-weight: 400;
						letter-spacing: 0.3px;
						line-height: 20px;
						border-radius: 8px;
						background-color: #f3f4f5;
					}
				}
			}
		}
	}
}
</style>
