<script>
    export default {
        data() {
            return {
                iconsImg: [
                    {
                        image: "buy-comics-digital-comics.png",
                        title: "DIGITAL COMICS",
                    },
                    {
                        image: "buy-comics-merchandise.png",
                        title: "DC MERCHANDISE",
                    },
                    {
                        image: "buy-comics-shop-locator.png",
                        title: "SUBSCRIPTION",
                    },
                    {
                        image: "buy-comics-shop-locator.png",
                        title: "COMIC SHOP LOCATOR",
                    },
                    {
                        image: "buy-dc-power-visa.svg",
                        title: "DC POWER VISA",
                    },
                ],
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
    <!-- <div class="bg-black">
        <h2 class="container"> Content goes here</h2>
    </div> -->

    <div class="bg-blue">
        <ul class="list-main container">
            <li v-for="image in iconsImg" class="align-items">
                <img class="img-main" :src="getImageUrl(image.image)" alt="">
                <span>{{ image.title }}</span>
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixins" as *;

    // .bg-black {
    //     background-color: $black;
    //     color: $white;
    //     padding: 30px 0;
    //     font-size: .6rem;
    // }

    .bg-blue {
        background-color: $primary-color;
        color: $white;
        padding: 30px;
    }

    .list-main {
        @include flex($justify: normal);
        list-style-type: none;
        gap: 30px;
    }

    .align-items {
        @include flex();
        gap: 20px;
        font-size: .6rem;
    }

    .img-main {
        height: 30px;
    }
</style>