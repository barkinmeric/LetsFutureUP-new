<template>
	<section class="adviceup">
		<social-head :title="$t('adviceup.title')" :description="$t('adviceup.desc')" />
		<div class="container">
			<div class="adviceup-body">
				<div class="left-part">
					<h2 class="title">{{ $t("adviceup.title") }}</h2>
					<p class="text">{{ $t("adviceup.desc") }}</p>
				</div>
				<div class="right-part">
					<nuxt-img
						format="jpg"
						class="image"
						draggable="false"
						src="/pages/index/hello-career/5.png"
						:alt="$t('adviceup.title')"
						height="458"
						width="608"
					/>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${$t("adviceup.title")} ${$t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: $t("adviceup.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.adviceup {
	margin: 112px 0 125px 0;
	.adviceup-body {
		display: flex;
		gap: 42px;
		justify-content: center;
		text-align: center;
		.left-part {
			.title {
				margin-top: 50px;
				font-size: 24px;
				font-weight: 900;
				letter-spacing: 1px;
				line-height: 30px;
				color: $titleColor;
				text-transform: uppercase;
			}
			.text {
				max-width: 608px;
				margin-top: 40px;
				font-size: 16px;
				font-weight: 400;
				letter-spacing: 0.1px;
				line-height: 34px;
				color: $textColor;
			}
		}
		.right-part {
			.image {
				border-radius: 8px;
			}
		}
	}
}
@media (max-width: 1200px) {
	.adviceup {
		margin: 10px 0 30px 0;
		.adviceup-body {
			display: grid;
			gap: 0;
			.left-part {
				.title {
					margin-top: 32px;
				}
			}
			.right-part {
				margin: 0 auto;
				.image {
					width: 100%;
					height: auto;
				}
			}
		}	
	}
}
</style>
