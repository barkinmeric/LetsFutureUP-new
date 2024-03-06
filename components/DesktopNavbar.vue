<template>
	<div class="desktop-navbar">
		<div class="container">
			<div class="flex-container">
				<div class="logo">
					<NuxtLink :to="`/${$locale}`"
						><nuxt-img draggable="false" src="/logo/logo.svg" alt="logo" height="50" width="200"
					/></NuxtLink>
				</div>
				<div class="content">
					<desktop-navbar-dropdown tab="nav.us" />
					<!-- <desktop-navbar-dropdown tab="nav.do" /> -->
					<desktop-navbar-dropdown tab="nav.career" />
					<a  target="_blank" class="dropdown-button" :href="$t('index.join-us.link')">{{ $t("index.join-us.button") }}</a>
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
	background-color: $backgroundColor;
	.flex-container {
		display: flex;
		align-items: center;
		height: 90px;
		.logo {
			margin: auto auto auto 0;
		}
		.content {
			margin: auto 0 auto auto;
			.dropdown-button {
				&:hover {
					color: $sideColor;
				}
				display: inline-block;
				padding: 35px 24px 15px 24px;
				height: 90px;
				line-height: 20px;
				font-weight: 700;
				letter-spacing: 0.3px;
				font-size: 1rem;
				border-radius: 8px;
				background-color: $backgroundColor;
				color: $titleColor;
				cursor: pointer;
			}
		}
	}
}
</style>
