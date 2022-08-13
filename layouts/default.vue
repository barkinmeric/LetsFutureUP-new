<template>
	<div>
		<locale-switcher />
		<desktop-navbar />
		<mobile-navbar />
		<nuxt />
		<all-footer />
	</div>
</template>

<script>
export default {
	head() {
		return this.$nuxtI18nHead({ addSeoAttributes: true });
	},
};
</script>

<style lang="scss">
.mobile-navbar {
	display: block;
}
.desktop-navbar {
	display: none;
}

@media (min-width: 996px) {
	.mobile-navbar {
		display: none;
	}
	.desktop-navbar {
		display: block;
	}
}
</style>
