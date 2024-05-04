<script>
    export default {
        data() {
            return {
                dcComics: [
                    {
                        title: "Characters",
                    },
                    {
                        title: "comics",
                    },
                    {
                        title: "Movies",
                    },
                    {
                        title: "TV",
                    },
                    {
                        title: "Games",
                    },
                    {
                        title: "Videos",
                    },
                    {
                        title: "News",
                    },
                ],
                shop: [
                    {
                        title: "Shop DC",
                    },
                    {
                        title: "Shop DC Collectibles",
                    },
                ],
                dc: [
                    {
                        title: "Terms Of Use",
                    },
                    {
                        title: "Privacy Policy (New)",
                    },
                    {
                        title: "Ad Choices",
                    },
                    {
                        title: "Advertising",
                    },
                    {
                        title: "Jobs",
                    },
                    {
                        title: "Subscriptions",
                    },
                    {
                        title: "Talent Workshops",
                    },
                    {
                        title: "CPSC Certificates",
                    },
                    {
                        title: "Ratings",
                    },
                    {
                        title: "Shop Help",
                    },
                    {
                        title: "Contact Us",
                    },
                ],
                sites: [
                    {
                        title: "DC",
                    },
                    {
                        title: "MAD Magazine",
                    },
                    {
                        title: "DC Kids",
                    },
                    {
                        title: "DC Universe",
                    },
                    {
                        title: "DC Power Visa",
                    },
                ],
                iconsFooter: [
                    {
                        image: "footer-facebook.png",
                    },
                    {
                        image: "footer-twitter.png",
                    },
                    {
                        image: "footer-youtube.png",
                    },
                    {
                        image: "footer-pinterest.png",
                    },
                    {
                        image: "footer-periscope.png",
                    },
                ]
            }
        },
        methods: {
            getImageUrl(imageName) {
                return new URL(`../assets/${imageName}`, import.meta.url).href;
            }
        }
    }
</script>

<template>
    <div class="bg-img">
        <div class="container footer">
            <div class="lists-footer">
                <div class="list-comics-shop">
                    <h2>DC COMICS</h2>
                    <ul class="lists">
                        <li v-for="item in dcComics">{{ item.title }}</li>
                    </ul>

                    <h2 class="shop-title">SHOP</h2>
                    <ul class="lists">
                        <li v-for="item in shop">{{ item.title }}</li>
                    </ul>
                </div>

                <div class="list-dc">
                    <h2>DC</h2>
                    <ul class="lists">
                        <li v-for="item in dc">{{ item.title }}</li>
                    </ul>
                </div>

                <div class="list-sites">
                    <h2>SITES</h2>
                    <ul class="lists">
                        <li v-for="item in sites">{{ item.title }}</li>
                    </ul>
                </div>
            </div>

            <div class="bg-logo"></div>
        </div>
    </div>

    <div class="btm-footer">
        <div class="container footer">
            <div>
                <button class="sign-up">SIGN-UP NOW!</button>
            </div>

            <div class="icons-footer">
                <h2>FOLLOW US</h2>
                <ul class="icons-footer">
                    <li v-for="image in iconsFooter">
                        <img class="icons" :src="getImageUrl(image.image)" alt="">
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixins" as *;
    
    .bg-img {
        background-image: url(/src/assets/footer-bg.jpg);
    }

    .footer {
        @include flex($justify: space-between);
    }

    .bg-logo {
        background-image: url(/src/assets/dc-logo-bg.png);
        width: 300px;
        background-size: cover;
    }

    .lists-footer {
        color: $white;
        font-size: .6rem;
        display: flex;
        gap: 30px;
        padding: 30px 0;
    }

    .shop-title {
        margin-top: 10px;
    }

    .lists {
        color: $gray;
        list-style-type: none;
        margin-top: 10px;
        line-height: 1.5;
    }

    .btm-footer {
        background-color: $dark-gray;
        padding: 30px 0;
    }

    .sign-up {
        background-color: $dark-gray;
        border: 1px solid $primary-color;
        color: $white;
        font-size: .6rem;
        padding: 10px;
    }

    .icons-footer {
        @include flex();
        gap: 20px;
        color: $primary-color;
        font-size: .6rem;
        list-style-type: none;
    }

    .icons {
        width: 30px;
    }
</style>