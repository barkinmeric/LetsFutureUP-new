<template>
	<div class="faq-collapsible">
		<button @click="toggleCollapsible = !toggleCollapsible" :class="{ active: toggleCollapsible }" type="button" class="collapsible">{{ title }}</button>
		<div class="content" v-if="toggleCollapsible">
			<div class="faq-collapsible-item">
				<div class="text">{{ text }}</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "FaqCollapsible",
	props: {
		title: String,
		text: String,
	},
	data() {
		return {
			toggleCollapsible: false,
		};
	},
};
</script>

<style lang="scss" scoped>
.faq-collapsible {
	.collapsible {
		background-color: #f3f4f5;
		color: $titleColor;
		cursor: pointer;
		padding: 16px;
		width: 100%;
		text-align: left;
		line-height: 24px;
		font-size: 1rem;
		font-weight: 900;
		letter-spacing: 0.3px;
		text-transform: uppercase;
		&:after {
			content: "\002B";
			color: black;
			font-size: 30px;
			font-weight: bold;
			float: right;
		}
		&:hover {
			background-color: #ccc;
		}
	}
	.active {
		background-color: #ccc;
		&:after {
			content: "\2212";
		}
	}
	.content {
		overflow: hidden;
		background-color: $backgroundColor;
		border: 1px solid #e7e9ec;
		.faq-collapsible-item {
			padding: 16px 32px;
			.text {
				line-height: 24px;
				font-size: 1rem;
				font-weight: 400;
				letter-spacing: 0.3px;
			}
		}
	}
}
</style>
