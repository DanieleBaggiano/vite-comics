<script setup>
    import { ref } from 'vue'

</script>

<template>
    <div class="bg-img">
        <div class="container footer">
            <div class="lists-footer">
                <div class="list-comics-shop">
                    <h2>DC COMICS</h2>
                    <ul class="lists">
                        <li>Characters</li>
                        <li>Comics</li>
                        <li>Movies</li>
                        <li>TV</li>
                        <li>Games</li>
                        <li>Videos</li>
                        <li>News</li>
                    </ul>

                    <h2 class="shop-title">SHOP</h2>
                    <ul class="lists">
                        <li>Shop DC</li>
                        <li>Shop DC Collectibles</li>
                    </ul>
                </div>

                <div class="list-dc">
                    <h2>DC</h2>
                    <ul class="lists">
                        <li>Terms Of Use</li>
                        <li>Privacy Policy (New)</li>
                        <li>Ad Choices</li>
                        <li>Advertising</li>
                        <li>Jobs</li>
                        <li>Subscriptions</li>
                        <li>Talent Workshops</li>
                        <li>CPSC Certificates</li>
                        <li>Ratings</li>
                        <li>Shop Help</li>
                        <li>Contact Us</li>
                    </ul>
                </div>

                <div class="list-sites">
                    <h2>SITES</h2>
                    <ul class="lists">
                        <li>DC</li>
                        <li>MAD Magazine</li>
                        <li>DC Kids</li>
                        <li>DC Universe</li>
                        <li>DC Power Visa</li>
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
                <img class="icons" src="/src/assets/footer-facebook.png" alt="">
                <img class="icons" src="/src/assets/footer-twitter.png" alt="">
                <img class="icons" src="/src/assets/footer-youtube.png" alt="">
                <img class="icons" src="/src/assets/footer-pinterest.png" alt="">
                <img class="icons" src="/src/assets/footer-periscope.png" alt="">
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    .bg-img {
        background-image: url(/src/assets/footer-bg.jpg);
        /* height: 300px; */
    }

    .footer {
        display: flex;
        justify-content: space-between;
    }

    .bg-logo {
        background-image: url(/src/assets/dc-logo-bg.png);
        /* height: 400px; */
        width: 300px;
        background-size: cover;
    }

    .lists-footer {
        color: white;
        font-size: .6rem;
        display: flex;
        gap: 30px;
        padding: 30px 0;
    }

    .shop-title {
        margin-top: 10px;
    }

    .lists {
        color: rgb(146 144 142);
        list-style-type: none;
        margin-top: 10px;
        line-height: 1.5;
    }

    .btm-footer {
        background-color: rgb(48 48 48);
        /* height: 30px; */
        padding: 30px 0;
    }

    .sign-up {
        background-color: rgb(48 48 48);
        border: 1px solid rgb(2 130 249);
        color: white;
        font-size: .6rem;
        padding: 10px;
    }

    .icons-footer {
        display: flex;
        align-items: center;
        gap: 20px;
        color: rgb(2 130 249);
        font-size: .6rem;
    }

    .icons {
        width: 30px;
    }
</style>