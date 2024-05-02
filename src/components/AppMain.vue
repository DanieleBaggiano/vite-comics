<script setup>
    import { ref } from 'vue'

</script>

<template>
    <div class="bg-black">
        <h2 class="container"> {{ "--> Content goes here <--" }} </h2>
    </div>

    <div class="bg-blue">
        <ul class="list-main container">
            <li class="align-items">
                <img class="img-main" src="/src/assets/buy-comics-digital-comics.png" alt="">
                <span>DIGITAL COMICS</span>
            </li>
            <li class="align-items">
                <img class="img-main" src="/src/assets/buy-comics-merchandise.png" alt="">
                <span>DC MERCHANDISE</span>
            </li>
            <li class="align-items">
                <img class="img-main" src="/src/assets/buy-comics-shop-locator.png" alt="">
                <span>SUBSCRIPTION</span>
            </li>
            <li class="align-items">
                <img class="img-main" src="/src/assets/buy-comics-shop-locator.png" alt="">
                <span>COMIC SHOP LOCATOR</span>
            </li>
            <li class="align-items">
                <img class="img-main" src="/src/assets/buy-dc-power-visa.svg" alt="">
                <span>DC POWER VISA</span>
            </li>
        </ul>
    </div>
</template>

<style lang="scss">
    .bg-black {
        background-color: black;
        color: white;
        padding: 30px 0;
        font-size: .6rem;
        /* text-align: center; */
    }

    .bg-blue {
        background-color: rgb(2 130 249);
        color: white;
        padding: 30px;
    }

    .list-main {
        display: flex;
        list-style-type: none;
        gap: 30px;
    }

    .align-items {
        display: flex;
        align-items: center;
        gap: 20px;
        font-size: .6rem;
    }

    .img-main {
        width: 30px;
    }
</style>