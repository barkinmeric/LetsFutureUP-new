<template>
	<footer>
		<div id="footer_menu">
			<div id="logo_wrapper">
				<img src="/pages/index/lfu.png" />
			</div>
			<div id="hello_carr">
				<p>Kariyerine merhaba DE</p>
				<ul>
					<li>Mentorluk Programı</li>
					<li>Öğrenci Değişim Programı</li>
					<li>StartUP</li>
					<li>WeTalk</li>
					<li>AdviceUP</li>
					<li>TalentUP</li>
				</ul>
			</div>
			<div id="who_r_we">
				<p>Biz Kimiz</p>
				<ul>
					<li>Hikayemiz</li>
					<li>Hakkımızda</li>
					<li>Proje Ekibi</li>
					<li>S.S.S</li>
				</ul>
			</div>
			<div id="what_v_do">
				<p>Neler Yapıyoruz</p>
				<ul>
					<li>Etkinlikler</li>
					<li>Duyurular</li>
				</ul>
			</div>
		</div>
		<div id="contact">
			<span>&copy; Let’s FutureUP 2022. Tüm Hakları Saklıdır.</span>
			<a href="mailto:humanresources@letsfutureup.com">humanresources@letsfutureup.com</a>
			<span id="social_media">
				<a href=""><img src="/pages/index/linkedin.svg" alt="" /></a>
				<a href=""><img src="/pages/index/facebook.svg" alt="" /></a>
				<a href=""><img src="/pages/index/instagram.svg" alt="" /></a>
			</span>
		</div>
	</footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
footer {
	background: $thirdColor;
	list-style-type: none;
	color: white;
	#footer_menu {
		display: grid;
		#logo_wrapper {
			grid-area: logoWrapper;
		}
		#hello_carr {
			grid-area: helloCarr;
		}
		#who_r_we {
			grid-area: whoRWe;
		}
		#what_v_do {
			grid-area: whatVDo;
		}
		grid-template-areas: "logoWrapper helloCarr whoRWe whatVDo";
		padding: 40px 5vw 20px 5vw;
		gap: 40px;
		@media (max-width: 800px) {
			grid-template-areas:
				"logoWrapper helloCarr"
				"whoRWe whatVDo";
			padding-right: 10vw;
		}
		p {
			font-style: normal;
			font-weight: 900;
			font-size: 1rem;
			line-height: 20px;
			letter-spacing: 0.6px;
		}
		ul {
			margin-top: 16px;
			font-style: normal;
			font-weight: normal;
			font-size: 1rem;
			line-height: 24px;
			letter-spacing: 0.6px;
			color: #ffffff;
		}
	}
	#contact {
		display: flex;
		flex-flow: row wrap;
		justify-content: space-between;
		align-items: center;
		padding: 20px 5vw;
		@media (max-width: 800px) {
			flex-direction: column !important;
		}
		a {
			text-decoration: none;
			color: white;
			margin-left: 15px;
			@media (max-width: 800px) {
				margin-top: 15px;
				margin-bottom: 15px;
			}
			&visited {
				color: white;
			}
		}
	}
}
</style>
