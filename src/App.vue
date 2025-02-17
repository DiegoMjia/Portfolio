<script setup lang="ts">
  import HeaderPortfolio from './components/HeaderPortfolio.vue'
  import BodyPortfolio from './components/BodyPortfolio.vue'
  import HabilitiesPort from './components/Habilities.vue'
  import FooterPage from './components/FooterPage.vue'
  import ContactMe from './components/ContactMe.vue'
  import AboutMe from './components/AboutMe.vue'
</script>

<template>
  <div>
    <HeaderPortfolio />
    <BodyPortfolio class="bodyPortfolio" />
    <HabilitiesPort />
    <AboutMe />
    <ContactMe />
    <FooterPage />
  </div>
</template>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
