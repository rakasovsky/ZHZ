<template>
    <v-layout class="comment-box">
    <v-container>
      <vue-disqus
        v-if="metadata"
        shortname="rakasovsky-netlify-app"
        :identifier="`rakasovsky-netlify-app-${metadata.title}`"
        :url="`https://rakasovsky.netlify.app/${metadata.url}`"
      ></vue-disqus>
        </v-container>
    </v-layout>
</template>

<script>
export default {
  computed: {
    metadata () {
      const metadata = this.$store.state.tutorials.slice()

      const tutorialMeta = metadata.filter((tutorial) => {
        return `/tutorials/${tutorial.url}` === this.$route.path
      })[0]

      return tutorialMeta
    }
  }
}
</script>