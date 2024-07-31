<script>
export default {
    data() {
        return {
            social: [
                {
                    img: "#",
                    url: "../assets/img/footer-facebook.png"
                },
                {
                    img: "#",
                    url: "../assets/img/footer-twitter.png"
                },
                {
                    img: "#",
                    url: "../assets/img/footer-youtube.png"
                },
                {
                    img: "#",
                    url: "../assets/img/footer-periscope.png"
                },
                {
                    img: "#",
                    url: "../assets/img/footer-periscope.png"
                }
            ]
        }
    }
}
</script>
<template lang="">
    <div class="bg-brown">
        <div class="container py-4">
            <div class="row">
                <div class="col-12 d-flex justify-content-between align-items-center">
                    <button class="text-white fw-bold p-2">SIGN-UP NOW!</button>
                    <div class="d-flex align-items-center">
                        <h4 class="m-0 me-3">FOLLOW US</h4>
                        <img v-for="(icon, index) in social" :key="'social-' + index" v-bind:src="icon.img" class="mx-2">
                    </div>                    
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .bg-brown {
        background-color: #303030;
    }
    button {
        background-color: #ffffff00;
        border: 2px solid #0282f9;
    }
    h4 {
        color:#0282f9
    }
</style>