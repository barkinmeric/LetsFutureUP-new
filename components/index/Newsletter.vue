<template>
	<div class="newsletter">
		<div class="container">
			<h1 class="newsletter-title">Duyurular & Etkinlikler</h1>
			<div class="newsletter-body">
				<div class="left-part">
					<nuxt-img format="jpg" src="/pages/index/slider/desktop/en/1.webp" height="392px" width="500px" alt="StartUP" draggable="false" loading="lazy" />
					<h2 class="card-title">Mentor & Mentee başvuruları başladı!</h2>
					<span class="card-tag">Duyurular</span>
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
	padding: 20px 10px 50px 10px;
	background: $backgroundColor;
	.newsletter-title {
		color: $titleColor;
		padding: 0px 0px 36px 0px;
		font-size: 2rem;
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
			position: relative;
			height: 392px;
			width: fit-content;
			.card-title {
				color: white;
				text-shadow: 2px 2px black;
				font-size: 1.5rem;
				font-weight: 900;
				letter-spacing: 0.6px;
				line-height: 34px;
				position: absolute;
				bottom: 26px;
				left: 20px;
			}
			.card-tag {
				height: 32px;
				width: 97px;
				padding: 6px 16px;
				text-align: center;
				font-size: 0.875rem;
				font-weight: 400;
				letter-spacing: 0.3px;
				line-height: 20px;
				border-radius: 8px;
				background-color: #f3f4f5;
				position: absolute;
				top: 24px;
				right: 24px;
			}
		}
		.right-part {
			display: grid;
			grid-template-columns: 100%;
			row-gap: 40px;
			margin-right: 9px;
			.right-card {
				display: flex;
				gap: 16px;
				img {
					height: 176px;
				}
				.card-desc {
					display: grid;
					grid-template-columns: 100%;
					.card-title {
						font-size: 1.125;
						font-weight: 900;
						letter-spacing: 0.6px;
						line-height: 34px;
					}
					.card-text {
						font-size: 0.875rem;
						font-weight: 400;
						letter-spacing: 0.6px;
						line-height: 20px;
					}
					.card-tag {
						height: 32px;
						width: 97px;
						padding: 6px 16px;
						text-align: center;
						font-size: 0.75rem;
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
@media (max-width: 1200px) {
	.newsletter {
		.newsletter-body {
			display: grid;
			gap: 0;
			img {
				max-width: 100%;
				width: 100%;
				height: auto;
			}
			.left-part {
				margin: 0 auto;
			}
			.right-part {
				margin-top: 30px;
			}
		}
	}
}
</style>
