<template>
	<section class="about-us">
		<social-head :title="$t('about.title')" :description="$t('index.desc')" />
		<div class="container">
			<div class="head">
				<div class="head-text">{{ $t("about.head.text") }}</div>
				<a  target="_blank" :href="$t('index.join-us.link')" class="button">{{ $t("about.head.button") }}</a>
			</div>
			<div class="body">
				<div v-for="item in $t('about.content')" :key="item.title">
					<h3 class="item-title">{{ item.title }}</h3>
					<p class="item-text">{{ item.text }}</p>
				</div>

				<div>
					<h3 class="item-title">{{ $t("about.list.title") }}</h3>
					<ul v-for="item in $t('about.list.text')" :key="item">
						<li class="list-text">
							<br />
							{{ item }}
						</li>
					</ul>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${$t("about.title")} ${$t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: $t("index.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.about-us {
	margin: 80px 0 127px 0;
	.head {
		text-align: center;
		margin: 20px 0;
		.head-text {
			margin: auto;
			max-width: 850px;
			font-size: 32px;
			font-weight: 900;
			letter-spacing: 0.3px;
			line-height: 34px;
			color: $titleColor;
			padding-bottom: 15px;
			@media (max-width: $mobile_bp) {
				font-size: 28px;
			}
		}
		.button {
			display: inline-block;
			margin: 24px 0 92px 0;
			padding: 18px 32px 18px 32px;
			background-color: $sideColor;
			font-size: 16px;
			font-weight: 700;
			letter-spacing: 0.3px;
			line-height: 20px;
			color: #ffffff;
			border-radius: 16px;
		
			&:hover {
				background: rgb(44, 28, 225);
			}
		}
	}
	.body {
		text-align: center;
		.item-title {
			color: #000;
			margin-bottom: 10px;
			text-transform: uppercase;
			font-size: 24px;
			font-weight: 900;
			letter-spacing: 0.3px;
			line-height: 20px;
			padding-bottom: 10px;
			@media (max-width: $mobile_bp) {
				font-size: 18px;
			}
		}
		.item-text {
			max-width: 824px;
			margin: 0 auto;
			color: #292929;
			margin-bottom: 100px;
			font-size: 16px;
			font-weight: 400;
			letter-spacing: 0.3px;
			line-height: 24px;
		}
		.list-text {
			max-width: 621px;
			margin: 0 auto;
			color: #292929;
			font-size: 16px;
			font-weight: 400;
			letter-spacing: 0.3px;
			line-height: 24px;
		}
	}
}
</style>
