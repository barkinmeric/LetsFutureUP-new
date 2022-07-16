<template>
	<div class="mobile-navbar-dropdown">
		<div class="flex-container" @click="toggleDropdown()">
			<h2 class="dropdown-button">{{ $t(`${tab}.title`) }}</h2>
			<div class="down-icon">
				<icon-angle-down color="black" width="24px" height="24px" />
			</div>
		</div>
		<div class="dropdown-content" v-show="isDropdownActive">
			<NuxtLink v-for="(item, index) in $t(`${tab}.content`)" :key="item" :to="localePath(toUrl($t(`${tab}.content`, 'en')[index]))">
				<h3 class="text">{{ item }}</h3>
			</NuxtLink>
		</div>
	</div>
</template>

<script>
export default {
	name: "MobileNavbarDropdown",
	props: {
		tab: String,
	},
	data() {
		return {
			isDropdownActive: false,
		};
	},
	methods: {
		toggleDropdown() {
			this.isDropdownActive = !this.isDropdownActive;
		},
		toUrl(text) {
			return text
				.toLowerCase()
				.replace(/ /gim, "-")
				.replace(/ğ/gim, "g")
				.replace(/ü/gim, "u")
				.replace(/ş/gim, "s")
				.replace(/ı/gim, "i")
				.replace(/ö/gim, "o")
				.replace(/ç/gim, "c");
		},
	},
	watch: {
		$route(to, from) {
			this.isDropdownActive = false;
		},
	},
};
</script>

<style lang="scss" scoped>
.mobile-navbar-dropdown {
	background-color: $backgroundColor;
	.flex-container {
		cursor: pointer;
		display: flex;
		align-items: center;
		.dropdown-button {
			height: 84px;
			width: 100%;
			padding: 24px 0 24px 16px;
			color: $titleColor;
			border-radius: 8px;
			line-height: 34px;
			font-weight: 900;
			font-size: 1.5rem;
			letter-spacing: 0.6px;
			cursor: pointer;
		}
		.down-icon {
			width: 24px;
			height: 24px;
			margin: 29px 16px 29px auto;
			cursor: pointer;
		}
		&:hover {
			color: $sideColor;
			border-radius: 8px;
			.dropdown-button {
				color: $sideColor;
			}
			.down-icon {
				svg {
					color: $sideColor;
				}
			}
		}
	}
	.dropdown-content {
		background-color: $backgroundColor;
		width: 100%;
		z-index: 1;
		border-radius: 8px;
		.text {
			color: $titleColor;
			height: 48px;
			padding: 14px 0 14px 32px;
			display: block;
			letter-spacing: 0.3px;
			line-height: 20px;
			font-size: 1rem;
			font-weight: 700;
		}
	}
}
</style>
