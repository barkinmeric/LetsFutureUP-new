<template>
	<section id="mentee-sec">
		<div id="text-side">
			<h3>{{ $t("mentorship.content[0].title") }}</h3>
			<article>{{ $t("mentorship.content[0].text") }}</article>
			<a :href="$t('index.join-us.link')" class="join-btn">{{ $t("index.join-us.button") }}</a>
		</div>
		<div id="img-side">
			<div></div>
		</div>
	</section>
</template>

<script>
export default {};
</script>

<style lang="scss" scope>
#mentee-sec {
	display: flex;
	flex-flow: row wrap;
	padding: 80px 0 122px 0;
	#img-side {
		width: 50%;
		div {
			width: 608px;
			height: 513px;
			background: url("/pages/mentorship-program/mentorStock.png");
			border-radius: 8px;
		}
		@media (max-width: $tablet_bp) {
			display: none;
		}
	}
	#text-side {
		width: 50%;
		text-align: center;
		h3 {
			max-width: 608px;
			height: 30px;
			font-style: normal;
			font-weight: 900;
			font-size: 24px;
			line-height: 30px;
			color: #000000;
			margin: auto;
			@media (max-width: $tablet_bp) {
				margin: auto;
			}
		}
		article {
			margin: 24px auto 0px auto;
			max-width: 608px;
			font-style: normal;
			font-weight: 400;
			font-size: 16px;
			line-height: 34px;
			text-align: center;
			letter-spacing: 0.1px;
			color: #000000;
			box-sizing: border-box;
		}
		.join-btn {
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			padding: 18px 32px;
			width: 176px;
			height: 56px;
			background: #2719cc;
			border-radius: 16px;
			margin: 24px auto 0px auto;
			color: white;
			font-style: normal;
			font-weight: 700;
			font-size: 16px;
			line-height: 20px;
		}
		@media (max-width: $tablet_bp) {
			width: 100%;
		}
	}
}
</style>
