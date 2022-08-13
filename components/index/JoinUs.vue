<template>
	<div class="join-us">
		<div class="container">
			<div class="join-body">
				<div class="left-part">
					<h1 class="title">Sen de aramıza katılmak ister misin?</h1>
					<p class="text">
						Sen de aramıza mentor, mentee veya ekip üyesi olarak katılmak istersen <br />
						yandaki butona tıklayarak form doldurabilirsin
					</p>
				</div>
				<div class="right-part">
					<a class="button" :href="$t('index.join-us.link')">{{ $t("index.join-us.button") }}</a>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "Subscribe",
};
</script>

<style lang="scss" scoped>
.join-us {
	background: #2719cc;
	padding: 24px;
	.join-body {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		align-items: center;
		.left-part {
			.title {
				margin: 0 0 8px 0;
				font-weight: 900;
				font-size: 20px;
				line-height: 25px;
				letter-spacing: 0.6px;
				color: #ffffff;
			}
			.text {
				font-weight: 400;
				font-size: 16px;
				line-height: 24px;
				letter-spacing: 0.3px;
				color: #ffffff;
			}
		}
		.right-part {
			.button {
				padding: 14px 24px;
				background: #ffffff;
				border-radius: 8px;
				font-weight: 700;
				font-size: 16px;
				line-height: 20px;
				letter-spacing: 0.6px;
				color: #222222;
			}
		}
	}
}
</style>
