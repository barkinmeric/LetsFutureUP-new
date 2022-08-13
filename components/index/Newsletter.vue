<template>
	<div class="newsletter">
		<div class="container">
			<h1 class="newsletter-title">{{ $t("events-announcements.title") }}</h1>
			<div class="newsletter-body">
				<div class="left-part">
					<nuxt-img
						format="jpg"
						class="image"
						draggable="false"
						:src="$t('events-announcements.content')[0].image"
						height="392px"
						width="500px"
						alt="StartUP"
						loading="lazy"
					/>
					<h2 class="card-title">{{ $t("events-announcements.content")[0].title }}</h2>
					<span class="card-tag">{{ $t("events-announcements.content")[0].type }}</span>
				</div>
				<div class="right-part">
					<div class="right-card" v-for="(item, i) in $t('events-announcements.content').slice(1, 3)" :key="i" :item="item">
						<nuxt-img
							format="jpg"
							class="image"
							:src="item.image"
							height="176px"
							width="176px"
							alt="StartUP"
							draggable="false"
							loading="lazy"
						/>
						<div class="card-desc">
							<h2 class="card-title">{{ item.title }}</h2>
							<p class="card-text">
								{{ truncate(item.text, 265) }}
							</p>
							<span class="card-tag">{{ item.type }}</span>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "Newsletter",
	methods: {
		toUrl(text) {
			return text
				.toLowerCase()
				.replace(/[`~!@#$%^&*()_|+\-=?;:'",.<>\{\}\[\]\\\/]/gi, "")
				.replace(/ /gim, "-")
				.replace(/--/gim, "-")
				.replace(/ğ/gim, "g")
				.replace(/ü/gim, "u")
				.replace(/ş/gim, "s")
				.replace(/ı/gim, "i")
				.replace(/ö/gim, "o")
				.replace(/ç/gim, "c");
		},
		truncate(str, len) {
			if (str.length > len && str.length > 0) {
				let new_str = str + " ";
				new_str = str.substr(0, len);
				new_str = str.substr(0, new_str.lastIndexOf(" "));
				new_str = new_str.length > 0 ? new_str : str.substr(0, len);
				return new_str + "...";
			}
			return str;
		},
	},
};
</script>

<style lang="scss" scoped>
.newsletter {
	padding: 0;
	margin-bottom: 100px;
	background: $backgroundColor;
	.newsletter-title {
		color: $titleColor;
		padding: 0px 0px 36px 0px;
		font-size: 2rem;
		font-weight: 900;
		letter-spacing: 0.6px;
		line-height: 40px;
	}
	.newsletter-body {
		display: flex;
		gap: 40px;
		.left-part {
			position: relative;
			height: 392px;
			width: fit-content;
			.image {
				user-select: none;
				border-radius: 8px;
			}
			.card-title {
				color: white;
				text-shadow: 2px 2px black;
				font-size: 1.5rem;
				font-weight: 900;
				letter-spacing: 0.6px;
				line-height: 34px;
				position: absolute;
				bottom: 26px;
				left: 20px;
			}
			.card-tag {
				height: 32px;
				width: 97px;
				padding: 6px 16px;
				text-align: center;
				font-size: 0.875rem;
				font-weight: 400;
				letter-spacing: 0.3px;
				line-height: 20px;
				border-radius: 8px;
				background-color: #f3f4f5;
				position: absolute;
				top: 24px;
				right: 24px;
			}
		}
		.right-part {
			display: grid;
			grid-template-columns: 100%;
			row-gap: 40px;
			margin-right: 9px;
			.right-card {
				display: flex;
				gap: 16px;
				.image {
					user-select: none;
					border-radius: 8px;
					height: 176px;
				}
				.card-desc {
					display: grid;
					grid-template-columns: 100%;
					.card-title {
						font-size: 1.125;
						font-weight: 900;
						letter-spacing: 0.6px;
						line-height: 34px;
					}
					.card-text {
						font-size: 0.875rem;
						font-weight: 400;
						letter-spacing: 0.6px;
						line-height: 20px;
					}
					.card-tag {
						height: 32px;
						width: 97px;
						padding: 6px 16px;
						text-align: center;
						font-size: 0.75rem;
						font-weight: 400;
						letter-spacing: 0.3px;
						line-height: 20px;
						border-radius: 8px;
						background-color: #f3f4f5;
					}
				}
			}
		}
	}
}
@media (max-width: 1200px) {
	.newsletter {
		.newsletter-body {
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
				margin-top: 30px;
				.image {
					max-width: 100%;
					width: 100%;
					height: auto;
				}
			}
		}
	}
}
</style>
