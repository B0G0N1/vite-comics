<script>
export default {
    data() {
        return {
            dcComics: [
                {
                    text: "characters",
                    url: "#"
                },
                {
                    text: "comics",
                    url: "#"
                },
                {
                    text: "movies",
                    url: "#"
                },
                {
                    text: "tv",
                    url: "#"
                },
                {
                    text: "games",
                    url: "#"
                },
                {
                    text: "videos",
                    url: "#"
                },
                {
                    text: "news",
                    url: "#"
                }
            ],
            shop: [
                {
                    text: "shop dc",
                    url: "#"
                },
                {
                    text: "shop dc collectibles",
                    url: "#"
                }
            ],
            dc: [
                {
                    text: "term of use",
                    url: "#"
                },
                {
                    text: "privacy policy (new)",
                    url: "#"
                },
                {
                    text: "ad choices",
                    url: "#"
                },
                {
                    text: "advertising",
                    url: "#"
                },
                {
                    text: "jobs",
                    url: "#"
                },
                {
                    text: "subscriptions",
                    url: "#"
                },
                {
                    text: "talent workshops",
                    url: "#"
                },
                {
                    text: "cpsc certificates",
                    url: "#"
                },
                {
                    text: "ratings",
                    url: "#"
                },
                {
                    text: "shop help",
                    url: "#"
                },
                {
                    text: "contact us",
                    url: "#"
                }
            ],
            sites: [
                {
                    text: "dc",
                    url: "#"
                },
                {
                    text: "mad magazine",
                    url: "#"
                },
                {
                    text: "dc kids",
                    url: "#"
                },
                {
                    text: "dc universe",
                    url: "#"
                },
                {
                    text: "dc power visa",
                    url: "#"
                },
            ]
        }
    }
}
</script>
<template lang="">
    <div class="top_footer">
        <div class="container py-4">
            <div class="row">
                <div class="col-2">
                    <h4 class="text-white mb-1">DC COMICS</h4>
                    <ul class="text-white list-unstyled">
                        <li v-for="(link, index) in dcComics" :key="'dcComics-' + index" class="text-capitalize">
                            <a :href=link.url class="text-decoration-none text-reset" >{{ link.text }}</a>
                        </li>
                    </ul>
                    <h4 class="text-white my-1">SHOP</h4>
                    <ul class="text-white list-unstyled">
                        <li v-for="(link, index) in shop" :key="'shop' + index" class="text-capitalize">
                            <a :href=link.url class="text-decoration-none text-reset" >{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-2">
                    <h4 class="text-white mb-1">DC</h4>
                    <ul class="text-white list-unstyled">
                        <li v-for="(link, index) in dc" :key="'dc-' + index" class="text-capitalize">
                            <a :href=link.url class="text-decoration-none text-reset" >{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-2">
                    <h4 class="text-white mb-1">SITES</h4>
                    <ul class="text-white list-unstyled">
                        <li v-for="(link, index) in sites" :key="'sites-' + index" class="text-capitalize">
                            <a :href=link.url class="text-decoration-none text-reset" >{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .top_footer {
        background-image: url("../assets/img/footer-bg.jpg");
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;

        .container {
            background-image: url("../assets/img/dc-logo-bg.png");
            background-position: right center;
            background-size: auto 130%;
            background-repeat: no-repeat;
        }

        a {
            font-size: 14px;
        }
    }
</style>