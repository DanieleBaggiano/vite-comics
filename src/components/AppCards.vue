<script>
    export default {
        data() {
            return {
                banner: [
                    {
                        image: "src/assets/jumbotron.jpg"
                    }
                ],
                cards: [
                    {
                        thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                        price: "$19.99",
                        series: "Action Comics",
                        type: "comic book",
                    },
                    {
                        thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                        price: "$3.99",
                        series: "American Vampire 1976",
                        type: "comic book",
                    },
                    {
                        thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                        price: "$16.99",
                        series: "Aquaman",
                        type: "graphic novel",
                    },
                    {
                        thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                        price: "$2.99",
                        series: "Batgirl",
                        type: "comic book",
                    },
                    {
                        thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                        price: "$3.99",
                        series: "Batman",
                        type: "comic book",
                    },
                    {
                        thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                        price: "$2.99",
                        series: "Batman Beyond",
                        type: "comic book",
                    },
                    {
                        thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                        price: "$3.99",
                        series: "Batman/Superman",
                        type: "comic book",
                    },
                    {
                        thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                        price: "$4.99",
                        series: "Batman/Superman Annual",
                        type: "comic book",
                    },
                    {
                        thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                        price: "$5.99",
                        series: "Batman: The Joker War Zone",
                        type: "comic book",
                    },
                    {
                        thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                        price: "$6.99",
                        series: "Batman: Three Jokers",
                        type: "comic book",
                    },
                    {
                        thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                        price: "$4.99",
                        series: "Batman: White Knight Presents: Harley Quinn",
                        type: "comic book",
                    },
                    {
                        thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                        price: "$16.99",
                        series: "Catwoman",
                        type: "graphic novel",
                    },
                ]
            }
        },
        methods: {
            getImagePath(img) {
                return new URL(`${img}`, import.meta.url).href;
            }
        }
    }
</script>

<template>
    <section>
        <div class="banner-container">
            <img class="banner" :src="banner[0].image" alt="">

            <div class="container">
                <button class="btn">CURRENT SERIES</button>
            </div>
        </div>

        <div class="bg-black">
            <div class="container-cards">
                <div class="cards" v-for="item in cards">
                    <img :src="getImagePath(item.thumb)" alt="">
                    <h2>{{ item.series }}</h2>
                </div>
                <button class="btn">LOAD MORE</button>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixins" as *;

    .banner-container {
        width: 100%;
        height: 40vh;
        object-fit: cover;
        overflow: hidden;

        .banner {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            top: 55%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: -1;
        }

        .btn {
            background-color: $primary-color;
            padding: 10px 50px;
            border: none;
            color: $white;
            font-weight: bold;
            position: absolute;
            bottom: 400px;
            cursor: pointer;
        }
    }

    .bg-black {
        background-color: $light-black;
        width: 100%;
    }

    .container-cards {
        width: 80%;
        height: 100%;
        margin: 0 auto;

        padding: 30px 0;
        @include flex($wrap: wrap);
        gap: 50px;

        .cards {
            width: calc(100% / 6 - 50px);
            height: 200px;
            object-fit: cover;

            img {
                height: 100%;
                width: 100%;
            }

            h2 {
                font-size: .6rem;
                color: $white;
                text-transform: uppercase;
                padding-top: 10px;
            }
        }

        .btn {
            background-color: $primary-color;
            padding: 10px 50px;
            border: none;
            color: $white;
            font-weight: bold;
            margin-top: 40px;
            font-size: .6rem;
            cursor: pointer;
        }
    }
</style>