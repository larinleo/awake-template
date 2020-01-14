<template>
  <div
    id="home-page"
    class="page-wrapper home-page"
  />
</template>

<script>
import { mapState } from 'vuex'
import { setPageData } from '../helper'

export default {
  name: 'HomePage',
  layout: 'home',
  head() {
    return {
      title: `Home | ${this.$siteConfig.siteName}`
    }
  },

  computed: {
    ...mapState(['title', 'subtitle', 'featureImage'])
  },
  fetch({ store, params }) {
    setPageData(store, { slug: 'home' })
  }
}
</script>

<style>
.home-page .under-subtitle {
  border-top: none;
}
</style>
