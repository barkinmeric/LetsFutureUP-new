<template>
	<section class="talentup">
		<social-head :title="$t('talentup.title')" :description="$t('talentup.desc')" />
		<div class="container">
			<div class="talentup-body">
				<div class="left-part">
					<nuxt-img
						format="jpg"
						class="image"
						draggable="false"
						src="/pages/talentup/img.png"
						:alt="$t('talentup.title')"
						height="491"
						width="608"
					/>
				</div>
				<div class="right-part">
					<h2 class="title">{{ $t("talentup.title") }}</h2>
					<p class="text">{{ $t("talentup.desc") }}</p>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("talentup.title")} ${this.$i18n.t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: this.$i18n.t("talentup.desc"),
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.talentup {
	margin: 82px 0 125px 0;
	.talentup-body {
		display: flex;
		gap: 38px;
		justify-content: center;
		text-align: center;
		.left-part {
			.image {
				border-radius: 8px;
			}
		}
		.right-part {
			.title {
				margin-top: 112px;
				font-size: 1.5rem;
				font-weight: 900;
				letter-spacing: 1px;
				line-height: 30px;
				color: $titleColor;
				text-transform: uppercase;
			}
			.text {
				margin-top: 40px;
				font-size: 1rem;
				font-weight: 400;
				letter-spacing: 0.1px;
				line-height: 34px;
				color: $textColor;
			}
		}
	}
}
@media (max-width: 1200px) {
	.talentup {
		margin: 10px 0 30px 0;
		.talentup-body {
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
				.title {
					margin-top: 32px;
				}
			}
		}
	}
}
</style>
