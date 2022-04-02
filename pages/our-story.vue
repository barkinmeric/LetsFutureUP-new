<template>
	<section class="our-story">
		<social-head :title="$t('story.title')" :description="$t('index.desc')" />
		<div class="container">
			<div class="our-story-body">
				<div class="left-part">
					<nuxt-img format="jpg" class="image" draggable="false" src="/pages/our-story/img.png" :alt="$t('story.title')" height="454" width="500" />
				</div>
				<div class="right-part">
					<h2 class="title">{{ $t("story.title") }}</h2>
					<div class="text-part">
						<p class="text" v-for="paragraph in $t('story.content').slice(0, 2)" :key="paragraph">{{ paragraph }}</p>
					</div>
				</div>
			</div>
			<p class="text" v-for="paragraph in $t('story.content').slice(2)" :key="paragraph">{{ paragraph }}</p>
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
					content: this.$i18n.t("story.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.our-story {
	margin: 100px 0 30px 0;
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
				font-size: 3rem;
				font-weight: 900;
				letter-spacing: 1px;
				line-height: 60px;
				color: $titleColor;
				text-transform: uppercase;
			}
			.text-part {
				margin-top: 128px;
				.text {
					font-size: 1rem;
					font-weight: 700;
					letter-spacing: 0.3px;
					line-height: 24px;
					color: $textColor;
				}
			}
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
