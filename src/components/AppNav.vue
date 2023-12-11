<script>
import { store } from "../store.js"
import register from "../debug.js"

export default {
    name: "AppComponent",
    data() {
        return {
            store,
            menuItems: [
                {
                    title: "Home",

                },
                {
                    title: "Pages",

                },
                {
                    title: "Portfolio",

                },
                {
                    title: "Blog",

                },
                {
                    title: "Shop",

                },
                {
                    title: "Elements",

                }

            ]
        }
    },
    methods: {

    },
    mounted() {

    }
}
</script>

<template>
    <nav class="navbar bg-white align-items-center menu">
        <div class="container-fluid">
            <img src="img/logo-sidearea-1.png" alt="">
            <form class="d-flex text-black" role="search">
                <span class="me-2" v-for="item in menuItems">
                    {{ item.title }}
                </span>
                <img src="/svg/svg-1.svg" alt="">
            </form>
        </div>
    </nav>
</template>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;

// ...qui eventuale SCSS di AppComponent
.menu {
    min-height: 6rem;
}
</style>