<template>
	<div class="mobile-navbar">
		<div class="container">
			<div class="flex-container">
				<div class="logo">
					<NuxtLink :to="`/${this.$i18n.locale}`"><nuxt-img draggable="false" src="/logo/logo.svg" alt="logo" width="140" height="35" /></NuxtLink>
				</div>

				<div class="mobile-menu-button" @click="toggleMobileMenu()" v-show="!isMobileMenuActive">
					<icon-bars width="24px" height="24px" color="black" />
				</div>

				<div class="mobile-menu-button" @click="toggleMobileMenu()" v-show="isMobileMenuActive">
					<icon-times width="24px" height="24px" color="black" />
				</div>
			</div>
			<div class="mobile-menu" v-show="isMobileMenuActive">
				<mobile-navbar-dropdown tab="nav.us" />
				<mobile-navbar-dropdown tab="nav.do" />
				<mobile-navbar-dropdown tab="nav.career" />
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "MobileNavbar",
	data() {
		return {
			isMobileMenuActive: false,
		};
	},
	methods: {
		toggleMobileMenu: function () {
			this.isMobileMenuActive = !this.isMobileMenuActive;
		},
	},
	watch: {
		$route(to, from) {
			this.isMobileMenuActive = false;
		},
	},
};
</script>

<style lang="scss" scoped>
.mobile-navbar {
	background-color: $mainColor;
	.flex-container {
		display: flex;
		align-items: center;
		height: 70px;
		.logo {
			margin: 17.5px auto 17.5px 16px;
		}
		.mobile-menu-button {
			width: 24px;
			height: 24px;
			margin: 23px 24px 23px auto;
			cursor: pointer;
		}
	}
}
</style>
