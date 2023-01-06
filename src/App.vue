<script setup>
import { RouterLink, RouterView } from 'vue-router'
import SitesysNavbar from './components/Sitesys/Global/SitesysNavbar/SitesysNavbar.vue'
import SitesysFooter from './components/Sitesys/Global/SitesysFooter/SitesysFooter.vue'
import ScrollToTop from './components/Sitesys/Global/ScrollToTop/ScrollToTop.vue'
</script>

<template>
  <div class="tracking-wide">
    <SitesysNavbar />
    <ScrollToTop class="bg-orange-400 hover:bg-orange-400/80" />
    <RouterView />
    <SitesysFooter />
  </div>
</template>

<style scoped></style>
