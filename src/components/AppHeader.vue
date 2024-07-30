<script>
export default {
    data(){
        return{
            links: [
                {
                    label: 'Characters',
                    url: '#',
                    current: false
                },
                {
                    label: 'Comics',
                    url: '#',
                    current: true
                },                
                    {
                    label: 'Movies',
                    url: '#',
                    current: false
                },                
                {
                    label: 'TV',
                    url: '#',
                    current: false
                },                
                {
                    label: 'Games',
                    url: '#',
                    current: false
                },                {
                    label: 'Collectibles',
                    url: '#',
                    current: false
                },                {
                    label: 'Videos',
                    url: '#',
                    current: false
                },                
                {
                    label: 'Fans',
                    url: '#',
                    current: false
                },                
                {
                    label: 'News',
                    url: '#',
                    current: false
                },                
                {
                    label: 'Shop',
                    url: '#',
                    current: false
                }
            ]
        }
    }
}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <div class="col-12 d-flex justify-content-between pt-3">
                <img src="../assets/img/dc-logo.png">
                <div class="d-flex list-unstyled align-items-center">
                    <div v-for="link, index in links" :key="index" :class="link.current ? 'active' : ''" class="d-flex align-items-center h-100 mx-2">
                        <a :href="link.url" class="text-decoration-none text-uppercase fw-bold">{{ link.label }}</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    a {
        color: darkgrey;
    }
    .active {
        border-bottom: 0.5rem solid #0282f9;
        a {
            color: #0282f9;
        }
    }
</style>