<script>
import AppHeader from './components/AppHeader.vue';
import AppMainContent from './components/AppMainContent.vue';
import AppPromotion from './components/AppPromotion.vue';

export default {
  components: {
    AppHeader,
    AppMainContent,
    AppPromotion
  }
}
</script>
<template lang="">
  <div>
    <AppHeader/>
    <AppMainContent/>
    <AppPromotion/>
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss';
</style>