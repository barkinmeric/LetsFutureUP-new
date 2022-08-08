<template>
	<div class="depSec" :id="id">
		<department-desc :secText="secText" :style="descOrderStyle" />
		<department-img :secImg="secImg" :style="imgOrderStyle" />
	</div>
</template>

<script>
export default {
	props: ["secData"],
	data() {
		return {
			id: this.secData.id,
			secText: this.secData.text,
			secImg: this.secData.imgs,
			descOrderStyle: [this.swap() ? { order: 2 } : { order: 1 }],
			imgOrderStyle: [this.swap() ? { order: 1 } : { order: 2 }],
		};
	},
	methods: {
		swap() {
			if (this.secData.index % 2 !== 0) {
				return true;
			}
		},
	},
};
</script>

<style lang="scss" scope>
.depSec {
	display: flex;
	justify-content: center;
	align-content: center;
	flex-flow: row wrap;
}
</style>
