<template>
	<div class="subscribe">
		<div class="container">
			<img class="image" src="/pages/index/subscribe/image.png" alt="subscribe-image" />
			<h1 class="title">Bültenimize Abone Ol</h1>
			<p class="text">
				Etkinliklerden haberdar olmak için bültenimize <br />
				abone olabilirsiniz.
			</p>
			<form id="form" action="#" method="post">
				<input type="email" placeholder="E-posta girin" name="email" class="input" />
				<input type="submit" value="Abone Ol" class="button" />
			</form>
		</div>
	</div>
</template>

<script>
export default {
	name: "Subscribe",
};
</script>

<style lang="scss" scoped>
.subscribe {
	text-align: center;
	position: relative;
	margin-bottom: 110px;
	.image {
		background-color: #343434;
		border-radius: 8px;
		width: 100%;
	}
	.title {
		color: white;
		position: absolute;
		top: 10%;
		left: 50%;
		transform: translate(-50%, 0);
		font-weight: 900;
		font-size: 2rem;
		line-height: 2.5rem;
		letter-spacing: 0.6px;
	}
	.text {
		color: white;
		position: absolute;
		top: 30%;
		left: 50%;
		transform: translate(-50%, 0);
		font-weight: 400;
		font-size: 1rem;
		line-height: 1.5rem;
		letter-spacing: 0.6px;
	}
	.input {
		background: rgba(255, 255, 255, 0.1);
		border-radius: 8px;
		width: 392px;
		height: 3rem;
		color: white;
		position: absolute;
		top: 55%;
		left: 50%;
		transform: translate(-50%, 0);
	}
	.button {
		padding: 0.9rem;
		border-radius: 8px;
		color: #222222;
		background-color: #ffffff;
		position: absolute;
		top: 70%;
		left: 50%;
		transform: translate(-50%, 0);
		font-weight: 700;
		font-size: 1rem;
		line-height: 1.25rem;
		letter-spacing: 0.6px;
	}
}
</style>
