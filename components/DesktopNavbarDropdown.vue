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
			color: $sideColor;
		}
	}
	.dropdown-button {
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
	.dropdown-content {
		display: none;
		width: 260px;
		position: absolute;
		top: 100%;
		left: 0;
		perspective: 1000px;
		background-color: $backgroundColor;
		border-radius: 8px;
		animation: growDown 300ms ease-in-out forwards;
		transform-origin: top center;
		// box-shadow: 0px 0px 5px 1px #00000030;
		// border: 1px solid #00000050;
		padding-top: 10px;
		padding-bottom: 10px;
		.text {
			width: 100%;
			height: 100%;
			padding: 14px 16px;
			color: $titleColor;
			line-height: 20px;
			font-size: 1rem;
			font-weight: 400;
			letter-spacing: 0.3px;
			&:hover {
				border-radius: 8px;
				// background-color: $sideColor;
				color: $sideColor;
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
