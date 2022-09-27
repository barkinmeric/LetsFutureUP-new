<template>
	<section class="mentorship-program">
		<social-head :title="$t('mentorship.title')" :description="$t('index.desc')" />
		<div class="container">
			<mentor-section />
			<ment-grid :mentGrid="$t('mentorship.years.2021-2022.mentors')" />
			<mentee-section />
			<ment-grid :mentGrid="$t('mentorship.years.2021-2022.mentees')" />
			<button @click="toggleCollapsible = !toggleCollapsible" :class="{ active: toggleCollapsible }" type="button" class="collapsible">
				{{ $t(`mentorship.years.2020-2021.title`) }}
			</button>
			<div class="content" v-if="toggleCollapsible">
				<div class="mentorship-collapsible-item">
					<div class="container">
						<div class="flex-container">
							<ment-grid :mentGrid="$t('mentorship.years.2020-2021.mentors')" />
						</div>
					</div>
				</div>
				<div class="mentorship-collapsible-item">
					<div class="container">
						<div class="flex-container">
							<ment-grid :mentGrid="$t('mentorship.years.2020-2021.mentees')" />
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("mentorship.title")} ${this.$i18n.t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: this.$i18n.t("mentorship.desc"),
				},
			],
		};
	},
	data() {
		return {
			toggleCollapsible: false,
		};
	},
};
</script>

<style lang="scss" scope>
.mentorship-program {
	.collapsible {
		background-color: #eee;
		color: #444;
		cursor: pointer;
		margin: 20px 0;
		padding: 20px;
		width: 100%;
		text-align: left;
		font-size: 15px;
		line-height: 30px;
		text-transform: uppercase;
		border-radius: 8px;
		&:after {
			content: "\002B";
			color: black;
			font-size: 30px;
			font-weight: bold;
			float: right;
			margin-left: 5px;
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
		padding: 0 18px;
		overflow: hidden;
		background-color: #f1f1f1;
	}
	.mentorship-collapsible-item {
		text-align: center;
		.title {
			display: inline-block;
			padding-top: 15px;
			color: black;
			font-weight: 500;
			font-size: 22px;
			border-bottom: 2px solid $sideColor;
			text-transform: uppercase;
		}
		.flex-container {
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
		}
	}
}
</style>
