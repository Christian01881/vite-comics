<template>
  <div>
    <AppHeader />
    <AppContent />
    <AppMain />
    <AppFooterLinks />
    <AppFooterSocial />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppMain from './components/AppMain.vue';
import AppFooterLinks from './components/AppFooterLinks.vue';
import AppFooterSocial from './components/AppFooterSocial.vue';
  export default {
    components: {
      AppHeader,
      AppContent,
      AppMain,
      AppFooterLinks,
      AppFooterSocial,
    }
  }
</script>

<style lang="scss" scoped>

</style>