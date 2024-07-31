<script>
import AppBottomFooterVue from './components/AppBottomFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMainContent from './components/AppMainContent.vue';
import AppPromotion from './components/AppPromotion.vue';
import AppTopFooter from './components/AppTopFooter.vue';
import AppBottomFooter from './components/AppBottomFooter.vue';
import AppJumbotron from './components/AppJumbotron.vue';

export default {
  components: {
    AppHeader,
    AppMainContent,
    AppPromotion,
    AppTopFooter,
    AppBottomFooter,
    AppJumbotron
  }
}
</script>
<template lang="">
  <div>
    <AppHeader/>
    <AppJumbotron/>
    <AppMainContent/>
    <AppPromotion/>
    <AppTopFooter/>
    <AppBottomFooter/>
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss';
</style>