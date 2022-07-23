<template>
	<section class="about-us">
		<social-head :title="$t('about.title')" :description="$t('index.desc')" />
		<div class="container">
			<div class="head">
				<div class="head-text">{{ $t("about.head.text") }}</div>
				<span class="button">{{ $t("about.head.button") }}</span>
			</div>
			<div class="body">
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
	margin: 80px 0 30px 0;
	.head {
		text-align: center;
		margin: 20px 0;
		.head-text {
			margin: auto;
			max-width: 850px;
			font-size: 1.5rem;
			font-weight: 900;
			letter-spacing: 0.3px;
			line-height: 34px;
			color: $titleColor;
		}
		.button {
			display: inline-block;
			margin: 24px 0 92px 0;
			padding: 18px 32px 18px 32px;
			background-color: $sideColor;
			font-size: 1rem;
			font-weight: 700;
			letter-spacing: 0.3px;
			line-height: 20px;
			color: #ffffff;
			border-radius: 16px;
		}
	}
	.body {
		.text {
			color: #292929;
			font-size: 16px;
			font-weight: normal;
			margin-bottom: 15px;
		}
		.title {
			display: inline-block;
			font-size: 20px;
			font-weight: 600;
			letter-spacing: 1px;
			color: #000;
			border-bottom: 3px solid $sideColor;
			margin-bottom: 20px;
			text-transform: uppercase;
		}
		.item-text {
			color: #292929;
			font-size: 16px;
			font-weight: normal;
			margin-bottom: 15px;
		}
		.item-title {
			font-size: 18px;
			font-weight: 500;
			letter-spacing: 1px;
			color: #000;
			margin-bottom: 10px;
			text-transform: uppercase;
		}
	}
}
</style>
