<template>
	<section id="intr_sec">
		<div id="text_side">
			<p id="call_to_action">Geleğini bugün planla, Kariyer yolculuğuna hemen başla!</p>
			<p id="description">
				Let’s FutureUP, gelecekteki kariyerlerine şimdiden merhaba demek isteyen gençlere, mentorluk ve eğitim programları ile yol gösteren
				uluslararası bir sosyal sorumluluk projesidir.
			</p>
			<div id="btns_wrapper">
				<button id="join_btn">Bize Katıl</button>
				<button id="vid_popup_btn">
					<label> </label>
					<img />
					<span>Videoyu İzle</span>
				</button>
			</div>
			<div id="partners">
				<p>İşbirlikçilerimiz</p>
				<img />
			</div>
		</div>
		<div id="img_side">
			<img />
		</div>
	</section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$tablet_bp: 1200px;
$mobile_bp: 600px;
#intr_sec {
	display: flex;
	background: #ecf4fc;
	flex-flow: row nowrap;
	box-sizing: border-box;
	padding: 0 10vw 90px 10vw;
	margin-bottom: 100px;
	@media (max-width: $mobile_bp) {
		padding: 20px;
	}
	#text_side {
		display: flexbox;
		width: 50%;
		@media (max-width: $tablet_bp) {
			width: 90%;
		}
		@media (max-width: $mobile_bp) {
			width: 100%;
		}
		#call_to_action {
			font-family: Mulish;
			font-style: normal;
			font-weight: 900;
			font-size: 3rem;
			line-height: 64px;
			letter-spacing: 1px;
			padding-top: 160px;
			color: #121f3d;
			@media (max-width: $mobile_bp) {
				font-size: 2.5rem;
				padding-top: 80px;
			}
		}
		#description {
			font-family: Mulish;
			font-style: normal;
			font-weight: normal;
			font-size: 1rem;
			line-height: 36px;
			margin-top: 25px;

			letter-spacing: 0.3px;

			color: #121f3d;
		}
		#btns_wrapper {
			display: flex;
			flex-direction: row;
			margin-top: 48px;

			#join_btn {
				flex-direction: row;
				justify-content: center;
				align-items: center;
				padding: 18px 32px;

				width: 187px;
				height: 60px;
				background: #2719cc;
				color: white;
				border-radius: 16px;
				@media (max-width: $mobile_bp) {
					width: 50%;
					height: 50%;
				}
			}
			#vid_popup_btn {
				display: flex;
				flex-direction: row;
				justify-content: center;
				align-items: center;
				padding: 18px 30px;
				background: #ecf4fc;
				width: 187px;
				height: 60px;

				/* Monochrome/1000 */
				border: 1px solid #121f3d;
				box-sizing: border-box;
				border-radius: 16px;

				margin-left: 16px;
				img {
					content: url("/pages/index/play_btn.svg");
				}
				span {
					margin-left: 7px;
				}
				@media (max-width: $mobile_bp) {
					width: 50%;
					height: 50%;
				}
			}
		}
		#partners {
			font-family: Mullish;
			margin-top: 10vw;
			@media (max-width: $mobile_bp) {
				margin-top: 20vw;
			}
			p {
				width: 155px;
				height: 22px;
				font-style: normal;
				font-weight: 900;
				font-size: 1.125rem;
				line-height: 23px;
				letter-spacing: 0.267703px;
				color: #121f3d;
				opacity: 0.5;
				@media (max-width: $mobile_bp) {
					font-size: 1rem;
				}
			}
			img {
				content: url("/pages/index/intr_partners.svg");
				margin-top: 20px;
				@media (max-width: $mobile_bp) {
					width: 75%;
					height: 75%;
				}
			}
		}
	}
	#img_side {
		width: 50%;
		img {
			content: url("/pages/index/intr_stock.png");
			$intr_stock_width: 90%;
			width: $intr_stock_width;
			height: $intr_stock_width * 1, 0894;
			float: right;
			margin-top: 110px;
		}
		@media (max-width: $tablet_bp) {
			display: none;
		}
	}
}
</style>
