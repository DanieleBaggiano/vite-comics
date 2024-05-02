<script setup>
    import { ref } from 'vue'

</script>

<template>
    <div class="container">
        <div class="header">
            <img class="logo-header" src="/src/assets/dc-logo.png" alt="">
            <ul class="list-header">
                <li>CHARACTERS</li>
                <li>COMICS</li>
                <li>MOVIES</li>
                <li>TV</li>
                <li>GAMES</li>
                <li>COLLECTIBLES</li>
                <li>VIDEOS</li>
                <li>FANS</li>
                <li>NEWS</li>
                <li>SHOP</li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss">
    .header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin: 10px;
        /* width: 70%; */
    }

    .logo-header {
        width: 60px;
    }

    .list-header {
        display: flex;
        column-gap: 20px;
        list-style-type: none;
        font-size: .6rem;
    }
</style>