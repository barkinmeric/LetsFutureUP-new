<template>
	<div class="desktop-navbar">
		<div class="container">
			<div class="flex-container">
				<div class="logo">
					<NuxtLink :to="`/${this.$i18n.locale}`"><nuxt-img draggable="false" src="/logo/logo.png" alt="logo" height="50" width="200" /></NuxtLink>
				</div>
				<div class="content">
					<span class="tabs">{{ $t("nav.us.title") }}</span>
					<span class="tabs">{{ $t("nav.do.title") }}</span>
					<span class="tabs">{{ $t("nav.career.title") }}</span>
					<span class="tabs">İletişim</span>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "DesktopNavbar",
};
</script>

<style lang="scss" scoped>
.desktop-navbar {
	.flex-container {
		display: flex;
		height: 110px;
		.logo {
			margin: 30px auto 30px 0;
		}
		.content {
			margin: 45px 0 45px auto;
			display: flex;
			gap: 48px;
			.tabs {
				font-size: 16px;
				font-weight: 700;
				letter-spacing: 0.3px;
				line-height: 20px;
			}
		}
	}
}
</style>
