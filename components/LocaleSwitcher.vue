<template>
	<div class="locale-switcher">
		<div class="container">
			<div class="grid-container">
				<div>
					<NuxtLink :to="!('name' in this.$route.params) ? switchLocalePath('tr') : '/tr'"
						><span :class="{ active: this.$i18n.locale === 'tr' }">TR</span></NuxtLink
					>
					/
					<NuxtLink :to="!('name' in this.$route.params) ? switchLocalePath('en') : '/en'"
						><span :class="{ active: this.$i18n.locale === 'en' }">EN</span></NuxtLink
					>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "LocaleSwitcher",
};
</script>

<style lang="scss" scoped>
.locale-switcher {
	width: 100%;
	height: 30px;
	background: $mainColor;
	color: #000;
	font-size: 0.75rem;
	line-height: 30px;
	.grid-container {
		display: grid;
		justify-content: end;
		margin-right: 16px;
		align-items: center;
		span {
			color: #000;
			transition: all ease 0.5s;
			cursor: pointer;
			&:hover {
				color: $sideColor;
			}
		}
		.active {
			color: $sideColor;
			font-weight: bold;
		}
	}
}
</style>
