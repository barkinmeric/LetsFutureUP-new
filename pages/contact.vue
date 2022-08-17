<template>
	<div class="container">
		<h2 id="title">{{ $t("contact.title") }}</h2>
		<form id="contact-form" action="#" method="post">
			<h3>{{ $t("contact.name") }}</h3>
			<input type="text" name="name" class="form-input" />
			<h3>{{ $t("contact.surname") }}</h3>
			<input type="text" name="name" class="form-input" />
			<h3>{{ $t("contact.mail") }}</h3>
			<input type="email" name="email" class="form-input" />
			<h3>{{ $t("contact.message") }}</h3>
			<textarea name="message" id="form-input-field"></textarea>
		</form>
	</div>
</template>

<script>
export default {
		beforeCreate() {
		this.$router.push('/' + this.$i18n.locale)
	},
};
</script>

<style lang="scss" scoped>
#title {
	font-style: normal;
	font-weight: 900;
	font-size: 24px;
	line-height: 30px;
	letter-spacing: 1px;
	color: #2719cc;
	color: $sideColor;
	margin-top: 103px;
	text-align: center;
}
#contact-form {
	margin: 32px auto 154px auto;
	width: 608px;
	@media (max-width: $mobile_bp) {
		width: 400px;
	}
	h3 {
		margin-top: 7px;
		height: 20px;
		font-style: normal;
		font-weight: 900;
		font-size: 16px;
		line-height: 20px;
		letter-spacing: 0.1px;
		color: #000000;
	}
	.form-input {
		width: 100%;
		height: 56px;
		background: $depNav_background;
		border: 1px solid #d0d2d8;
		box-sizing: border-box;
		border-radius: 8px;
		margin-top: 7px;
	}
	#form-input-field {
		width: 100%;
		height: 218px;
		background: $depNav_background;
		border: 1px solid #d0d2d8;
		box-sizing: border-box;
		border-radius: 8px;
		resize: none;
		margin-top: 7px;
	}
}
</style>
