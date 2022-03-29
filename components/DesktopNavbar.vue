<template>
	<div class="desktop-navbar">
		<div class="container">
			<div class="flex-container">
				<div class="logo">
					<NuxtLink :to="`/${this.$i18n.locale}`"><nuxt-img draggable="false" src="/logo/logo.svg" alt="logo" height="50" width="200" /></NuxtLink>
				</div>
				<div class="content">
					<desktop-navbar-dropdown tab="nav.us" />
					<desktop-navbar-dropdown tab="nav.do" />
					<desktop-navbar-dropdown tab="nav.career" />
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
	background-color: $mainColor;
	.flex-container {
		display: flex;
		height: 90px;
		.logo {
			margin: auto auto auto 0;
		}
		.content {
			margin: auto 0 auto auto;
		}
	}
}
</style>
