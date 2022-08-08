<template>
	<div class="container">
		<dep-selection-bar @scroll-to-sec="ScrollToSec" />
		<dep-sections v-for="(secData, i) in depSectionContents" :key="i" :secData="secData"/>
	</div>
</template>
<script>
export default {
	head() {
		return {
			title: `Let's FutureUP ${this.$i18n.t("team.title")} ${this.$i18n.t("url")}`,
			meta: [
				{
					hid: "description",
					name: "description",
					content: this.$i18n.t("team.desc"),
				},
			],
		};
	},
	data() {
		return {
			depSectionContents: [
				{	
					index: 0,
					id: "humanRsr",
					text: {
						title: "İNSAN KAYNAKLARI",
						description:
							"Let’s FutureUP Mentorluk Programı ve proje ekip üyesi alım sürecini organize eder, mülakat yapar ve olumlu adayların oryantasyon sürecini yönetir. Öğrencilerin gelişimlerine yönelik eğitimler organize eder. Aylık E-Bülten hazırlanmasında rol oynar. Mentorluk Programına dahil olan öğrencilerin ve ekip üyelerinin devamlılığını takip eder. Proje ekip üyelerinin motivasyonlarının yüksek tutulması ve birbirlerini daha yakından tanıyabilmeleri adına kaynaşma etkinlikleri düzenler. WeTALK etkinliklerinin ve eğitimlerin içerik yazılarının hazırlanmasında Sosyal Medya ve Dijital Pazarlama Departmanı ile çalışır.",
					},
					imgs: ["grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png"]
				},
				{
					index: 1,
					id: "corCom",
					text: {
						title: "KURUMSAL İLETİŞİM DEPARTMANI",
						description:
							"Projede yer alan Mentorluk Programı, Kariyerine MerhabaDE! Öğrenci Gelişim Programı ve WeTALK etkinliklerine yönelik olarak üst düzey yöneticilerle iletişime geçerek mentor/eğitmen/konuşmacı olmaları için teklifte bulunur, toplantılar düzenleyerek projeyi tanıtır. Bu etkinliklerin organize edilmesinde ve paydaşlara duyurulmasında rol oynar. Sponsorluk çalışmaları yapar. Üniversite kulüpleriyle iletişime geçerek tanışma toplantıları düzenler.",
					},
					imgs: ["grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png"]
				},
				{
					index: 2,
					id: "busStr",
					text: {
						title: "İŞ & STRATEJİ GELİŞTİRME DEPARTMANI",
						description:
							"Let’s FutureUP projesinin misyonu ve vizyonu doğrultusunda stratejilerin geliştirilmesine destek vererek projenin hedeflerine ulaşması için inovatif fikirler ortaya koyar. Bu kapsamda projede bulunan departmanların yeni fikirler üretmesinde ve bu fikirlerin hayata geçirilmesinde liderlik eder. Yeni fikirlerin projeye nasıl entegre edilebileceği konusunda tüm departmanlar ile koordine bir şekilde çalışır.",
					},
					imgs: ["grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png"]
				},
				{
					index: 3,
					id: "forAf",
					text: {
						title: "DIŞ İLİŞKİLER DEPARTMANI",
						description:
							"Projede yer alan Mentorluk Programı, Kariyerine MerhabaDE! Öğrenci Gelişim Programı ve WeTALK etkinliklerinin içeriklerine yönelik olarak uluslararası şirketlerin yurt dışı bölümünde çalışan üst düzey yöneticilerle iletişime geçerek mentor/eğitmen/konuşmacı olmaları için teklifte bulunur, toplantılar düzenleyerek projeyi tanıtır. Bu etkinliklerin organize edilmesinde ve paydaşlara duyurulmasında rol oynar. Projeyi uluslararası bir konuma getirmek üzere yabancı öğrencilere ulaşabilmek için yurt dışındaki üniversite kulüpleriyle iletişime geçerek tanışma toplantıları düzenler.",
					},
					imgs: ["grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png"]
				},
				{
					index: 4,
					id: "socMed",
					text: {
						title: "SOSYAL MEDYA VE DİJİTAL PAZARLAMA DEPARTMANI",
						description:
							"Let’s FutureUP Projesi’nin sosyal medya hesaplarının etkin bir şekilde kullanılmasını sağlar. Aynı zamanda projenin ulusal ve uluslararası kitlelere ulaşmasında rol alır. Sosyal medya hesaplarında paylaşılmak üzere gönderiler ve içerikler hazırlar. WeTALK etkinliklerinin ve eğitimlerin duyurulmasını sağlar.",
					},
					imgs: ["grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png"]
				},
				{
					index: 5,
					id: "startUp",
					text: {
						title: "STARTUP DEPARTMANI",
						description:
							"StartUP Ekibi, projemizin ilerleyen dönemlerinde gerçekleştireceğimiz girişim tabanlı etkinlikler için hazırlıklar yapar. Bu ekip, genelde web sitemizin kurulumu, iyileştirilmesi, ilerleyişi, gelişimi ve yönetimi üzerine çalışmalar gerçekleştirir. Ayrıca projeyi yöneten programların kodlarının yazılmasından ve dijitale aktarılmasından sorumludur.",
					},
					imgs: ["grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png", "grayPlaceholder.png"]
				},
			],
		};
	},
	methods: {
		ScrollToSec(id) {
			document.getElementById(id).scrollIntoView();
		},
	},
};
</script>

<style lang="scss" scope></style>
