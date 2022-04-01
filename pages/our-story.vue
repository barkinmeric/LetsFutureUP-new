<template>
	<section class="our-story">
		<social-head :title="$t('story.title')" :description="$t('index.desc')" />
		<div class="container">
			<div class="flex-container">
				<div class="left-part">
					<nuxt-img format="jpg" class="image" draggable="false" src="/pages/our-story/img.png" :alt="$t('story.title')" height="454" width="500" />
				</div>
				<div class="right-part">
					<h2 class="title">{{ $t("story.title") }}</h2>
					<p class="text" v-for="paragraph in $t('story.content')" :key="paragraph">{{ paragraph }}</p>
				</div>
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
	margin: 100px 0 30px 0;
	.flex-container {
		display: flex;
		gap: 40px;
		justify-content: center;
		text-align: center;
		.left-part {
			height: 454px;
			width: fit-content;
			.image {
				border-radius: 8px;
			}
		}
		.right-part {
			.text {
				// margin-bottom: 10px;
				font-size: 1rem;
				font-weight: 700;
				letter-spacing: 0.3px;
				line-height: 24px;
				color: $textColor;
			}
			.title {
				font-size: 3rem;
				font-weight: 900;
				letter-spacing: 1px;
				line-height: 60px;
				color: $titleColor;
				text-transform: uppercase;
			}
		}
	}
}
@media (max-width: 1200px) {
	.our-story {
		.grid-container {
			display: grid;
			gap: 0;
			.left-part {
				margin: 0 auto;
				.image {
					max-width: 100%;
					width: 100%;
					height: auto;
				}
			}
			.right-part {
				margin-top: 30px;
			}
		}
	}
}
</style>
