<template>
	<section id="mentor-sec">
		<div id="img-side">
			<div></div>
		</div>
		<div id="text-side">
			<h3>MENTOR</h3>
			<article>
				Let’s FutureUP projesindeki mentorlar, sektöre dair bilgi ve becerilerini geliştirmek isteyen öğrencilere/menteelere proje planıyla
				paralel olarak yol gösteren, deneyimlerini paylaşan, öğretirken öğrenen ve rehberlik eden kişilerdir. Let’s FutureUP ekibi tarafından
				alanında uzman kişiler detaylı bir şekilde araştırılır ve ilgili kişilerin mentorluk başvurusu alınır. Seçilen her mentorun
				sorumluluğuna bir mentee verilir ve proje süresince menteesi ile görüşme yapması beklenir. Bu görüşmelerde mentorlar menteelerini en
				iyi şekilde kariyer yolculuklarına hazırlar
			</article>
			<button class="join-btn">Bize Katıl</button>
		</div>
	</section>
</template>

<script>
export default {};
</script>

<style lang="scss" scope>
#mentor-sec {
	display: flex;
	flex-flow: row wrap;
	padding: 80px 0 122px 0;
	#img-side {
		width: 50%;
		div {
			width: 608px;
			height: 513px;
			background: url("@/static/pages/mentorship-program/menteeStock.png");
			border-radius: 8px;
		}
		@media (max-width: $tablet_bp) {
			display: none;
		}
	}
	#text-side {
		width: 50%;
		text-align: center;
		padding: 100px 0 0 0;
		.join-btn {
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			padding: 18px 32px;
			width: 176px;
			height: 56px;
			background: #2719cc;
			border-radius: 16px;
			margin: auto;
			margin-top: 24px;
			color: white;
			font-style: normal;
			font-weight: 700;
			font-size: 16px;
			line-height: 20px;
		}
		h3 {
			width: 608px;
			height: 30px;
			font-style: normal;
			font-weight: 900;
			font-size: 24px;
			line-height: 30px;
			color: #000000;
			@media (max-width: $tablet_bp) {
				margin: auto;
			}	
		}
		article {
			margin-top: 24px;
			width: 608px;
			height: 238px;
			font-style: normal;
			font-weight: 400;
			font-size: 16px;
			line-height: 34px;
			letter-spacing: 0.1px;
			color: #000000;
			@media (max-width: $tablet_bp) {
				margin: auto;
			}	
		}
		@media (max-width: $tablet_bp) {
			width: 100%;
			margin: auto;
		}
	}
}
</style>
