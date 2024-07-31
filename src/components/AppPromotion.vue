<script>
export default {
    data() {
        return {
            promotions: [
                {
                    img: "/images/buy-comics-digital-comics.png",
                    text: "digital comics"
                },
                {
                    img: "/images/buy-comics-merchandise.png",
                    text: "dc merchandise"
                },
                {
                    img: "/images/buy-comics-shop-locator.png",
                    text: "subscription"
                },
                {
                    img: "/images/buy-comics-subscriptions.png",
                    text: "comic shop locator"
                },
                {
                    img: "/images/buy-dc-power-visa.svg",
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
                <div v-for="(item, index) in promotions" :key="'prom-' + index" class="col text-white d-flex justify-content-center align-items-center">
                    <img :src="item.img" class="me-2">
                    <p class="m-0 text-uppercase fs-5">{{ item.text }}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .bg-azure {
        background-color: #0282f9;
    }
    img {
        height: 50px;
    }
</style>