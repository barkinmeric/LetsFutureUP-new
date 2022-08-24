<template>
	<section id="intr-wrp">
		<div id="intr_sec" class="container">
			<div id="text_side">
				<p id="call_to_action">{{ $t("index.introduction.title") }}</p>
				<p id="description">{{ $t("index.introduction.text") }}</p>
				<div id="btns_wrapper">
					<a id="join_btn" :href="$t('index.join-us.link')">{{ $t("index.join-us.button") }}</a>
					<button id="vid_popup_btn" @click="showVideo = true">
						<label> </label>
						<img />
						<span>{{ $t("index.introduction.video-btn") }}</span>
					</button>
				</div>
				<div id="partners">
					<p>{{ $t("index.partner.title") }}</p>
					<a href="#partner"><img /></a>
				</div>
			</div>
			<div id="img_side">
				<img />
			</div>
		</div>
		<video-popup v-if="showVideo" :closeVideo="closeVideo" />
	</section>
</template>

<script>
export default {
	data() {
		return {
			showVideo: false,
		};
	},
	methods: {
		closeVideo() {
			this.showVideo = false;
		},
	},
};
</script>

<style lang="scss" scoped>
$tablet_bp: 1200px;
$mobile_bp: 600px;
#intr-wrp {
	background: #ecf4fc;
	#intr_sec {
		display: flex;
		flex-flow: row nowrap;
		box-sizing: border-box;
		padding: 0 0 90px 0;
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
				font-size: 52px;
				line-height: 64px;
				letter-spacing: 1px;
				padding-top: 160px;
				color: #121f3d;
				@media (max-width: $mobile_bp) {
					font-size: 38px;
					padding-top: 40px;
					line-height: 48px;
				}
			}
			#description {
				font-family: Mulish;
				font-style: normal;
				font-weight: normal;
				font-size: 18px;
				line-height: 36px;
				margin-top: 25px;
				letter-spacing: 0.3px;
				color: #121f3d;
				@media (max-width: $mobile_bp) {
					font-size: 14px;
					line-height: 36px;
				}
			}
			#btns_wrapper {
				display: flex;
				flex-direction: row;
				margin-top: 48px;
				font-size: 16px;
				#join_btn {
					display: flex;
					flex-direction: row;
					justify-content: center;
					align-items: center;
					padding: 18px 32px;
					width: 187px;
					min-height: 60px;
					background: #2719cc;
					color: white;
					border-radius: 16px;
					@media (max-width: $mobile_bp) {
						width: 50%;
						height: 50%;
					}
					&:hover {
						background: rgb(44, 28, 225);
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
					min-height: 60px;
					cursor: pointer;

					/* Monochrome/1000 */
					border: 1px solid #121f3d;
					box-sizing: border-box;
					border-radius: 16px;

					margin-left: 16px;
					&:hover {
						background: rgb(250, 250, 250);
					}

					&:active {
						background: white;
					}
					img {
						content: url("/pages/index/introduction/play_btn.svg");
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
					content: url("/pages/index/introduction/intr_partners.svg");
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
				content: url("/pages/index/introduction/intr_stock.png");
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
}
</style>
