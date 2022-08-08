<template>
	<li class="event-card">
		<div class="event-img-ctn">
			<nuxt-img format="jpg" draggable="false" class="img" :src="item.image" :alt="item.title" height="176" width="176" />
		</div>
		<article class="evt-article">
			<div class="art-ctn-wrap">
				<NuxtLink :to="`${localePath('announcements')}/${toUrl(item.title)}`">
					<h2 class="evt-hdr">{{ item.title }}</h2>
				</NuxtLink>
				<p class="evt-par">{{ truncate(item.text, 200) }}</p>
			</div>
			<div class="article-bottom-sec">
				<span class="evt-btn-date-wrapper">
					<button class="events-button">{{ $t("announcements.title") }}</button>
					<span class="date-notat"> {{ item.date }} </span>
				</span>
				<span class="more-link">{{ $t("announcements.more") }}</span>
			</div>
		</article>
	</li>
</template>

<script>
export default {
	props: ["item"],
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
.event-card {
	max-width: 608px;
	display: flex;
	flex-flow: row nowrap;
	display: flex;
	align-content: center;
	border: 1px solid #d0d2d8;
	border-radius: 8px;
	margin: 32px 40px 8px 0;
	padding: 16px;
	.event-img-ctn {
		padding-right: 16px;
		display: flex;
		flex-flow: column nowrap;
		justify-content: flex-end;
		.img {
			max-width: 176px;
			max-height: 176px;
			border-radius: 8px;
			height: 208px;
		}
	}
	.evt-article {
		display: flex;
		flex-flow: column nowrap;
		justify-content: space-between;
		.art-ctn-wrap {
			.evt-par {
				font-family: "Mulish";
				font-style: normal;
				font-weight: 400;
				font-size: 14px;
				line-height: 20px;
				letter-spacing: 0.6px;
			}
		}
		.article-bottom-sec {
			display: flex;
			flex-flow: row nowrap;
			justify-content: space-between;
			align-items: center;
			.evt-btn-date-wrapper {
				display: flex;
				flex-flow: row nowrap;
				align-items: center;
				.events-button {
					margin-right: 8px;
					display: flex;
					flex-direction: row;
					justify-content: center;
					align-items: center;

					padding: 6px 16px;
					gap: 10px;
					width: 97px;
					height: 32px;
					border-radius: 8px;

					color: #ffffff;
					background: rgba(18, 31, 61, 0.5);
					backdrop-filter: blur(31px);
				}
				.date-notat {
					width: 79px;
					height: 20px;

					font-family: "Mulish";
					font-style: normal;

					font-weight: 700;
					font-size: 14px;
					line-height: 20px;

					letter-spacing: 0.3px;
					color: #888f9e;
				}
			}
			.more-link {
				width: 56px;
				height: 20px;
				font-family: "Mulish";
				font-style: normal;
				font-weight: 900;
				font-size: 14px;
				line-height: 20px;
				letter-spacing: 0.6px;
				color: #cf253f;
				text-decoration: none;
				margin-right: 10px;
				:visited {
					color: inherit;
				}
			}
		}
	}
}
</style>
