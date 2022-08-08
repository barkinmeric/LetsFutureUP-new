<template>
	<div class="hello-career-card">
		<div class="card-item">
			<div class="card-head">
				<nuxt-img format="jpg" :src="item.image" height="260px" width="392px" alt="StartUP" draggable="false" loading="lazy" />
			</div>
			<div class="card-body">
				<NuxtLink :to="localePath(toUrl($t('index.hello-career.content', 'en')[index].title))"
					><h5>{{ item.title }}</h5>
				</NuxtLink>
				<p>{{ truncate(item.text, 165) }}</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "HelloCareerCard",
	props: ["item", "index"],
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
.hello-career-card {
	height: 400px;
	width: 392px;
	margin: 0 auto 66px auto;
	.card-item {
		display: grid;
		grid-template-columns: 100%;
		justify-content: center;
		background: white;
		border-radius: 10px;
		.card-head {
			height: 260px;
			width: 392px;
			img {
				user-select: none;
				border-radius: 16px;
			}
		}
		.card-body {
			display: grid;
			grid-template-columns: 100%;
			text-align: center;
			justify-content: center;
			h5 {
				display: inline-block;
				font-size: 1.125rem;
				font-weight: 900;
				letter-spacing: 0.3px;
				line-height: 28px;
				color: $titleColor;
				padding: 16px 0px 8px 0px;
			}
			p {
				font-size: 0.875rem;
				font-weight: 400;
				letter-spacing: 0.3px;
				line-height: 24px;
				color: $textColor;
			}
		}
	}
}
</style>
