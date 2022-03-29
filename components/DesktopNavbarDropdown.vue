<template>
	<div class="desktop-navbar-dropdown">
		<h2 class="dropdown-button">{{ $t(`${tab}.title`) }}</h2>
		<ul class="dropdown-content">
			<li v-for="(item, index) in $t(`${tab}.content`)" :key="item">
				<NuxtLink :to="localePath(toUrl($t(`${tab}.content`, 'en')[index]))">
					<h3 class="text">{{ item }}</h3>
				</NuxtLink>
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: "DesktopNavbarDropdown",
	props: {
		tab: String,
	},
	methods: {
		toUrl(text) {
			return text.toLowerCase().replace(/ /gim, "-").replace(/ğ/gim, "g").replace(/ü/gim, "u").replace(/ş/gim, "s").replace(/ı/gim, "i").replace(/ö/gim, "o").replace(/ç/gim, "c");
		},
	},
};
</script>

<style lang="scss" scoped>
.desktop-navbar-dropdown {
	position: relative;
	display: inline-block;
	z-index: 15;
	&:hover {
		.dropdown-content {
			display: block;
		}
		.dropdown-button {
			border-color: $titleColor;
			background-color: $titleColor;
			color: $mainColor;
		}
	}
	.dropdown-button {
		padding: 35px 24px 15px 24px;
		height: 90px;
		line-height: 20px;
		font-weight: 700;
		letter-spacing: 0.3px;
		font-size: 16px;
		border: 1px solid;
		border-radius: 8px;
		border-color: $mainColor;
		background-color: $mainColor;
		color: $titleColor;
		cursor: pointer;
	}
	.dropdown-content {
		display: none;
		width: fit-content;
		min-width: 100%;
		position: absolute;
		top: 100%;
		left: 0;
		perspective: 1000px;
		background-color: $mainColor;
		animation: growDown 300ms ease-in-out forwards;
		transform-origin: top center;
		border: 1px solid;
		border-radius: 8px;
		border-color: $mainColor;
		.text {
			white-space: nowrap;
			line-height: 25px;
			width: 100%;
			font-size: 12px;
			font-weight: 400;
			letter-spacing: 1px;
			color: $titleColor;
			padding: 12px 16px;
			&:hover {
				border: 1px solid;
				border-radius: 8px;
				border-color: $titleColor;
				background-color: $titleColor;
				color: $mainColor;
			}
		}
	}
}
@keyframes growDown {
	0% {
		transform: scaleY(0);
	}
	80% {
		transform: scaleY(1.1);
	}
	100% {
		transform: scaleY(1);
	}
}
</style>
