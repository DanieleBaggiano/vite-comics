<script>
    export default {
        data() {
            return {
                menuItems: [
                    {
                        title: "CHARACTERS",
                        active: false,
                    },
                    {
                        title: "MOVIES",
                        active: true,
                    },
                    {
                        title: "TV",
                        active: false,
                    },
                    {
                        title: "GAMES",
                        active: false,
                    },
                    {
                        title: "COLLECTIBLES",
                        active: false,
                    },
                    {
                        title: "VIDEOS",
                        active: false,
                    },
                    {
                        title: "FANS",
                        active: false,
                    },
                    {
                        title: "NEWS",
                        active: false,
                    },
                    {
                        title: "SHOP",
                        active: false,
                    },
                ]
            }
        },
    }
</script>

<template>
    <div class="container-header">
        <div class="header container">
            <img class="logo-header" src="/src/assets/dc-logo.png" alt="Logo di DC Comics">
            <ul class="list-header">
                <li v-for="item in menuItems" :class="{ active: item.active}">
                    <a href="">{{ item.title }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/mixins" as *;
    @use "../style/partials/variables" as *;

    .container-header {
        background-color: $white;
        width: 100%;
    }

    .header {
        @include flex(row, space-between, center);
    }

    .logo-header {
        width: 80px;
        padding: 10px;
    }

    .list-header {
        @include flex();
        column-gap: 20px;
        list-style-type: none;
        font-size: .6rem;
        font-weight: bold;
        height: 80px;

        li {
            &.active {
                border-bottom: 4px solid $primary-color;
                height: 100%;
                display: flex;
                align-items: center;

                a {
                    color: $primary-color;
                }
            }
        }
        
        a {
            text-decoration: none;
            color: $black
        }
    }
</style>