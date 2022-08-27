<template>
	<section class="our-story">
		<social-head :title="$t('story.title')" :description="$t('index.desc')" />
		<div class="container">
			<div class="our-story-body">
				<div class="left-part">
					<nuxt-img
						format="jpg"
						class="image"
						draggable="false"
						src="/pages/our-story/img.png"
						:alt="$t('story.title')"
						height="454"
						width="500"
					/>
				</div>
				<div class="right-part">
					<h2 class="title">{{ $t("story.title") }}</h2>
					<div class="text-part">
						<p class="text">{{ $t("story.content")[0] }}</p>
						<br />
						<p class="text">{{ $t("story.content")[1] }}</p>
					</div>
				</div>
			</div>
			<div class="bottom-part">
				<p class="text">{{ $t("story.content")[2] }}</p>
				<p class="saying">{{ $t("story.saying")[0] }}</p>
				<p class="author">{{ $t("story.saying")[1] }}</p>
				<p class="bottom-text">{{ $t("story.content")[3] }}</p>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("story.title")} ${this.$i18n.t("url")}`,
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
.our-story {
	margin: 100px 0 256px 0;
	.our-story-body {
		display: flex;
		gap: 40px;
		justify-content: center;
		text-align: center;
		.left-part {
			height: 100%;
			width: fit-content;
			.image {
				border-radius: 8px;
			}
		}
		.right-part {
			.title {
				font-size: 24px;
				font-weight: 900;
				letter-spacing: 1px;
				line-height: 60px;
				color: $titleColor;
				text-transform: uppercase;
			}
			.text-part {
				margin-top: 128px;
				.text {
					font-size: 16px;
					font-weight: 700;
					letter-spacing: 0.3px;
					line-height: 24px;
					color: $textColor;
				}
			}
		}
	}
	.bottom-part {
		text-align: center;
		margin-top: 70px;
		.text {
			font-size: 16px;
			font-weight: 400;
			letter-spacing: 0.3px;
			line-height: 24px;
			color: $textColor;
		}
		.saying {
			margin: 48px auto 16px auto;
			max-width: 700px;
			font-size: 24px;
			font-weight: 900;
			letter-spacing: 1px;
			line-height: 60px;
			color: #b8bcc5;
		}
		.author {
			margin: 0 auto 48px auto;
			max-width: 700px;
			font-size: 16px;
			font-weight: 400;
			letter-spacing: 0.3px;
			line-height: 20px;
			color: #b8bcc5;
		}
		.bottom-text {
			max-width: 850px;
			margin: 0 auto 0 auto;
			font-size: 16px;
			font-weight: 400;
			letter-spacing: 0.3px;
			line-height: 24px;
			color: $textColor;
		}
	}
}
@media (max-width: 1200px) {
	.our-story {
		margin: 10px 0 30px 0;
		.our-story-body {
			display: grid;
			gap: 0;
			.left-part {
				height: 100%;
				margin: 0 auto;
				.image {
					max-width: 100%;
					width: 100%;
					height: auto;
				}
			}
			.right-part {
				.text-part {
					margin-top: 64px;
				}
			}
		}
	}
}
</style>
