<template>
    <div id="app">
        <Header />   
        <nuxt/>
        <Footer />
    </div>
</template>

<script>
import Header from "@/components/Header"
import Footer from "@/components/Footer"

export default {
  components: {
            Header,
            Footer
        },  
  computed: {
    meta () {
      return [
        { charset: 'utf-8' },
        {
          name: 'viewport',
          content: 'width=device-width, initial-scale=1, maximum-scale=1 shrink-to-fit=no'
        },
        { hid: 'description', name: 'description', content: 'Главная' }
      ]
    }
  },

  head () {
    const canonical = `https://mysite.com${this.$route.path
      .toLowerCase()
      .replace(/\/$/, '')}`
    return {
      meta: [
        ...this.meta

      ],
      script: [
       
      ],
      link: [{ rel: 'canonical', href: canonical }]
    }
  }
}
</script>

<style>
    /* body {
    display: flex;
    flex-direction: column;
    display: grid;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
    overflow-x: hidden;
    width: 100%;
} */
</style>