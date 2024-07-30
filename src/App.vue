<script>
import AppHeader from './components/AppHeader.vue';
import AppMainContent from './components/AppMainContent.vue';

export default {
  components: {
    AppHeader,
    AppMainContent
  }
}
</script>
<template lang="">
  <div>
    <AppHeader/>
    <AppMainContent/>
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss';
</style>