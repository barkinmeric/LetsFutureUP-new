<template>
	<div class="mentor-card">
		<div class="mentor-card-inner" :class="{ mentor_card_sizing: isCollapsed }">
			<div class="mentor">
				<div class="img_ctn">
					<nuxt-img
						format="jpg"
						class="image"
						draggable="false"
						:src="mentor.image"
						height="392px"
						width="500px"
						:alt="mentor.name"
						loading="lazy"
					/>
				</div>
				<div class="info_ctn">
					<p class="profile_name">{{ mentor.name }}</p>
					<p class="profile_place">{{ mentor.place }}</p>
					<p class="profile_pos">{{ mentor.position }}</p>
				</div>
				<div class="quote_ctn">
					<p :class="{ quote_text: isCollapsed }">{{ mentor.text }}</p>
				</div>
			</div>
			<button class="collapse-btn" @click="isCollapsed = !isCollapsed">{{ mentor.button }}</button>
		</div>
	</div>
</template>

<script>
export default {
	props: ["mentor"],
	data() {
		return {
			isCollapsed: true,
		};
	},
};
</script>

<style lang="scss" scoped>
.mentor-card {
	text-align: center;
	padding-bottom: 20px;
	.mentor_card_sizing {
		min-height: 420px;
		max-height: 420px;
	}
	.mentor-card-inner {
		display: flex;
		flex-flow: column nowrap;
		.mentor {
			max-width: 286px;
			min-width: 286px;
			margin: 0 auto auto auto;
			.img_ctn {
				.image {
					width: 284px;
					height: 202px;
					border-radius: 8px;
				}
			}
			.info_ctn {
				padding-top: 25px;
				font-style: normal;
				font-weight: normal;
				font-size: 18px;
				line-height: 23px;

				text-align: center;
				letter-spacing: 0.6px;
				// color: white;

				.profile_name {
					font-weight: 900;
				}
				.profile_place {
					padding-top: 6px;
					font-size: 18px;
					font-weight: 600;
				}
				.profile_pos {
					padding-top: 6px;
					font-size: 16px;
					font-weight: 400;
				}
			}
			.quote_ctn {
				padding-top: 23px;
				font-style: normal;
				font-weight: normal;
				font-size: 14px;
				line-height: 24px;
				letter-spacing: 0.3px;
				color: #596277;
				.quote_text {
					max-height: 55px;
					overflow: hidden;
				}
			}
		}
		.collapse-btn {
			background-color: transparent;
			font-family: "Mulish";
			font-style: normal;
			font-weight: 700;
			font-size: 14px;
			line-height: 24px;
			text-align: center;
			letter-spacing: 0.6px;
			color: #2719cc;
		}
	}
}
</style>
