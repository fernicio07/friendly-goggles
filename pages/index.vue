<template>
  <section>
    <SiteNavbar />
    <MainContent />
    <SiteFooter />
  </section>
</template>

<script>
import MainContent from '../components/main/MainContent.vue'
import SiteFooter from '../components/shared/SiteFooter.vue'
import SiteNavbar from '../components/shared/SiteNavbar.vue'

export default {
  components: {
    MainContent,
    SiteFooter,
    SiteNavbar,
  },
}
</script>
