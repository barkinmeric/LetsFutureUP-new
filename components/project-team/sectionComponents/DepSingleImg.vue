<template>
	<div id="secSingleImg" :style="{ backgroundImage: `url(${require('@/static/pages/project-team/' + img)})` }"></div>
</template>

<script>
export default {
	props: ["img"],
};
</script>

<style lang="scss" scope>
#secSingleImg {
	width: 176px;
	height: 200px;
	margin: 20px;
}
</style>
