<script>
    import cardsArray from '../assets/cards';

    export default {
        data() {
            return {
                banner: [
                    {
                        image: "src/assets/jumbotron.jpg"
                    }
                ],
                cardsArray,
            }
        },
        props: {
            image: String,
            title: String,
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
                <div class="cards" v-for="card in cardsArray">
                    <img :src="card.thumb" alt="">
                    <h2>{{ card.series }}</h2>
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
            height: 100px;
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