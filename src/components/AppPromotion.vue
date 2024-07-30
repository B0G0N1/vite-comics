<script>
export default {
    data() {
        return {
            promotions: [
                {
                    img: "../assets/img/dc-logo.png ",
                    text: "digital comics"
                },
                {
                    img: "../assets/img/buy-comics-merchandise.png",
                    text: "dc merchandise"
                },
                {
                    img: "../assets/img/buy-comics-shop-locator.png",
                    text: "subscription"
                },
                {
                    img: "../assets/img/buy-comics-subscriptions.png",
                    text: "comic shop locator"
                },
                {
                    img: "../assets/img/buy-dc-power-visa.svg",
                    text: "dc power visa"
                },
            ]
        }
    }
}
</script>
<template lang="">
    <div class="bg-azure">
        <div class="container">
            <div class="row p-3">
                <div v-for="(item, index) in promotions" :key="'prom-' + index" class="col text-white">
                    <div class="d-flex justify-content-center align-items-center">
                        <img :src="item.img">
                        <p class="m-0 text-uppercase fs-5">{{ item.text }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .bg-azure {
        background-color: #0282f9;
    }
</style>