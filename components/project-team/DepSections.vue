<template>
	<div class="depSec" :id="secData.id">
		<div id="depDesc" :style="descOrderStyle">
			<h2>{{ secData.title }}</h2>
			<article>{{ secData.text }}</article>
		</div>

		<div id="depImg" :style="imgOrderStyle">
			<div id="secSingleImg" v-for="(img, i) in secData.content" :key="i">
				<nuxt-img format="jpg" class="image" draggable="false" :src="img.image" :alt="img.name" height="200" width="176" />
				<p class="name">{{ img.name }}</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	props: ["secData"],
	data() {
		return {
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
	margin-bottom: 150px;
	#depDesc {
		font-style: normal;
		text-align: center;
		letter-spacing: 0.3px;
		width: 50%;
		padding: 10px;
		@media (max-width: 1400px) {
			width: 100%;
			order: 1 !important;
			padding: 0px;
		}
		@media (max-width: $mobile_bp) {
			width: 100%;
			order: 1 !important;
			padding: 0px;
		}
		h2 {
			margin: 0px auto 20px auto;
			width: 90%;
			font-size: 28px;
		}
		article {
			width: 90%;
			margin: auto;
			font-size: 16px;
		}
	}
	#depImg {
		padding: 0 20px 20px 20px 20px;
		display: flex;
		flex-flow: row wrap;
		justify-content: center;
		align-items: center;
		#secSingleImg {
			margin: 20px;
			text-align: center;
			.image {
				border-radius: 8px;
			}
			.name {
				font-style: normal;
				font-weight: 900;
				font-size: 18px;
				line-height: 23px;
			}
		}
		@media (max-width: 1400px) {
			min-width: 650px;
			order: 2 !important;
		}
		@media (max-width: $mobile_bp) {
			min-width: 550px;
			order: 2 !important;
		}
	}
}
</style>
