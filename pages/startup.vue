<template>
	<section class="startup">
		<social-head :title="$t('startup.title')" :description="$t('startup.desc')" />
		<div class="container">
			<div class="startup-body">
				<div class="left-part">
					<h2 class="title">{{ $t("startup.title") }}</h2>
					<p class="text">{{ $t("startup.desc") }}</p>
				</div>
				<div class="right-part">
					<nuxt-img
						format="jpg"
						class="image"
						draggable="false"
						src="/pages/index/hello-career/4.png"
						:alt="$t('startup.title')"
						height="471"
						width="606"
					/>
				</div>
			</div>

			<div class="text-section" v-for="item in $t('startup.content')" :key="item.title">
				<h3 class="item-title">{{ item.title }}</h3>
				<p class="item-text">{{ item.text }}</p>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${$t("startup.title")} ${$t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: $t("startup.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.startup {
	margin: 92px 0 105px 0;
	text-align: center;
	.startup-body {
		display: flex;
		gap: 42px;
		justify-content: center;
		margin-bottom: 138px;
		.right-part {
			.image {
				border-radius: 8px;
			}
		}
		.left-part {
			.title {
				margin-top: 71px;
				font-size: 24px;
				font-weight: 900;
				letter-spacing: 1px;
				line-height: 30px;
				color: $titleColor;
				text-transform: uppercase;
			}
			.text {
				margin-top: 40px;
				font-size: 16px;
				font-weight: 400;
				letter-spacing: 0.1px;
				line-height: 34px;
				color: $textColor;
				max-width: 608px;
			}
		}
	}
	.text-section {
		margin-bottom: 70px;
		.item-title {
			color: #000;
			margin-bottom: 40px;
			text-transform: uppercase;
			font-size: 24px;
			font-weight: 900;
			letter-spacing: 0.3px;
			line-height: 30px;
		}
		.item-text {
			max-width: 824px;
			margin: 0 auto;
			color: #292929;
			margin-bottom: 100px;
			font-size: 16px;
			font-weight: 400;
			letter-spacing: 0.1px;
			line-height: 34px;
		}
	}
}
@media (max-width: 1200px) {
	.startup {
		margin: 10px 0 30px 0;
		.startup-body {
			display: grid;
			gap: 0;
			.left-part {
				margin: 0 auto;
				.image {
					width: 100%;
					height: auto;
				}
			}
			.right-part {
				display: none;
			}
		}
	}
}
</style>
