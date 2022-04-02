<template>
	<div class="container">
		<mentor-section/>
		<mentee-section/>
	</div>
</template>

<script>
import mentorSection from '@/components/mentorshipProgram/MentorSection.vue';
import MenteeSection from '../components/mentorshipProgram/MenteeSection.vue';
export default {
  components: { mentorSection, MenteeSection },
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
};
</script>

<style lang="scss" scope>

</style>
