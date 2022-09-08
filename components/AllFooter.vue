<template>
	<section class="footer">
		<div class="footer-inner container">
			<div id="footer_menu">
				<div id="logo_wrapper">
					<img src="/pages/footer/logo.svg" />
				</div>
				<div id="who_r_we">
					<p>{{ $t("nav.us.title") }}</p>
					<ul>
						<li v-for="(item, index) in $t('nav.us.content')" :key="item">
							<NuxtLink :to="localePath(toUrl($t('nav.us.content', 'en')[index]))">
								<h3 class="text">{{ item }}</h3>
							</NuxtLink>
						</li>
					</ul>
				</div>
				<!-- <div id="what_v_do">
					<p>{{ $t("nav.do.title") }}</p>
					<ul>
						<li v-for="(item, index) in $t('nav.do.content')" :key="item">
							<NuxtLink :to="localePath(toUrl($t('nav.do.content', 'en')[index]))">
								<h3 class="text">{{ item }}</h3>
							</NuxtLink>
						</li>
					</ul>
				</div> -->
				<div id="hello_carr">
					<p>{{ $t("nav.career.title") }}</p>
					<ul>
						<li v-for="(item, index) in $t('nav.career.content')" :key="item">
							<NuxtLink :to="localePath(toUrl($t('nav.career.content', 'en')[index]))">
								<h3 class="text">{{ item }}</h3>
							</NuxtLink>
						</li>
					</ul>
				</div>
			</div>
			<div id="contact">
				<a href="mailto:humanresources@letsfutureup.com">humanresources@letsfutureup.com</a>
				<span id="copyright-cont">&copy; {{ $t("nav.copyright") }}</span>
				<span id="social_media">
					<a href=""><img src="/pages/footer/linkedin.svg" alt="" /></a>
					<a href=""><img src="/pages/footer/facebook.svg" alt="" /></a>
					<a href=""><img src="/pages/footer/instagram.svg" alt="" /></a>
				</span>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: "AllFooter",
	methods: {
		toUrl(text) {
			return text
				.toLowerCase()
				.replace(/ /gim, "-")
				.replace(/ğ/gim, "g")
				.replace(/ü/gim, "u")
				.replace(/ş/gim, "s")
				.replace(/ı/gim, "i")
				.replace(/ö/gim, "o")
				.replace(/ç/gim, "c");
		},
	},
};
</script>

<style lang="scss" scoped>
.footer {
	background: $thirdColor;
	.footer-inner {
		margin: auto;
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
			padding: 40px 0 20px 0;
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
				.text {
					font-style: normal;
					font-weight: normal;
					font-size: 1rem;
					line-height: 24px;
					letter-spacing: 0.6px;
					color: #ffffff;
				}
			}
		}
		#contact {
			display: flex;
			flex-flow: row wrap;
			justify-content: space-between;
			align-items: center;
			padding: 20px 0;
			@media (max-width: 1200px) {
				flex-direction: column !important;
				gap: 15px;
			}
			a {
				text-decoration: none;
				color: white;
				margin-left: 15px;
				&visited {
					color: white;
				}
			}
			#copyright-cont {
				margin-right: 200px;
				@media (max-width: 1200px) {
					margin: auto;
				}
			}
		}
	}
}
</style>
