<template>
	<section class="about-us">
		<div class="container">
			<div class="body">
				<h2 class="title">Let’s FutureUP, gençlere mentorluk ve eğitim programları ile yol gösteren uluslararası bir sosyal sorumluluk projesidir.</h2>
				<button class="join-btn">Bize Katıl</button>
				<div v-for="item in $t('about.content')" :key="item.title">
					<h3 class="item-title">{{ item.title }}</h3>
					<ul v-if="item.title == `Hedeflerimiz` || item.title == 'Our goals'">
						<li class="item-text" v-for="text in item.text" :key="text">
							{{ text }}
						</li>
					</ul>
					<p class="text" v-else>{{ item.text }}</p>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("about.title")} ${this.$i18n.t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: this.$i18n.t("index.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.about-us {
	margin: auto;
	text-align: center;
	width: 824px;
	padding: 81px 0 126px 0;
	.body {
		.title {
			text-align: center;
			font-style: normal;
			font-weight: 900;
			font-size: 24px;
			line-height: 34px;
			letter-spacing: 0.3px;
			color: #000000;
			margin-top: 81px;
		}
		.join-btn {
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			padding: 18px 32px;
			width: 176px;
			height: 56px;
			background: #2719CC;
			border-radius: 16px;
			margin: auto;
			margin-top: 24px;
			color: white;
			font-style: normal;
			font-weight: 700;
			font-size: 16px;
			line-height: 20px;
		}
		.text {
			color: #292929;
			font-size: 16px;
			font-weight: normal;
			margin-bottom: 15px;
			margin-top: 24px;
		}
		.item-text {
			color: #292929;
			font-size: 16px;
			font-weight: normal;
			margin-top: 36px;
		}
		.item-title {
			font-style: normal;
			font-weight: 900;
			font-size: 16px;
			line-height: 20px;
			letter-spacing: 0.3px;
			color: #000000;
			margin-top: 100px;
		}
	}
}
</style>
