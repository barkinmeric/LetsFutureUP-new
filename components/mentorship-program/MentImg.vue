<template>
	<div id="sec-single-img">
		<nuxt-img format="jpg" class="image" draggable="false" :src="img.image" :alt="$t('story.title')" height="260" width="287" />
	</div>
</template>

<script>
export default {
	props: ["img"],
};
</script>

<style lang="scss" scope>
#secSingleImg {
	width: 287px;
	height: 260px;
	margin: 10px;
}
</style>
