<script>
import AppComicSeries from './AppComicSeries.vue';

export default {
    components: {
        AppComicSeries
    }
}
</script>
<template lang="">
    <div class="bg-black">
        <div class="container position-relative text-center">
            <div class="current_series position-absolute translate-middle-y fw-bold text-white p-2">CURRENT SERIES</div>
            <AppComicSeries/>
            <button class="text-white fw-bold py-2 px-5 border-0 mb-4">LOAD MORE</button>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .current_series, button {
        background-color: #0282f9;
    }
</style>