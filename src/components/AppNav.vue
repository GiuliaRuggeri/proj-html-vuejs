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
                    submenu: [
                        {
                            title: "prova"
                        },
                        {
                            title: "prova1"
                        }
                    ]

                },
                {
                    title: "Pages",
                    submenu: [
                        {
                            title: "prova"
                        },
                        {
                            title: "prova1"
                        },
                        {
                            title: "prova2"
                        }
                    ]
                },
                {
                    title: "Portfolio",

                },
                {
                    title: "Blog",

                },
                {
                    title: "Shop",
                    submenu: [
                        {
                            title: "prova"
                        },
                        {
                            title: "prova1"
                        },
                        {
                            title: "prova2"
                        }
                    ]
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

                <div class="dropdown" v-for="item in menuItems">
                    <span class="me-4 item" type="button" aria-expanded="false">
                        {{ item.title }}
                    </span>

                    <ul class="dropdown-menu w-100" v-if="item.submenu">
                        <li v-for="submenu in item.submenu">
                            {{ submenu.title }}
                        </li>
                    </ul>
                </div>

                <!-- <span class="me-4 item" v-for="item in menuItems">
                    {{ item.title }}

                    <ul v-if="item.submenu">
                        <li v-for="submenu in item.submenu">
                            {{ submenu.title }}
                        </li>
                    </ul>
                </span> -->
                <img data-bs-toggle="offcanvas" data-bs-target="#offcanvasScrolling" src="/svg/svg-1.svg" alt="">
            </form>
        </div>
    </nav>
    <div class="offcanvas offcanvas-end" data-bs-scroll="true" data-bs-backdrop="false" tabindex="-1"
        id="offcanvasScrolling" aria-labelledby="offcanvasScrollingLabel">
        <div class="offcanvas-header">
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
            <div class="d-flex flex-column justify-content-center align-items-center">
                <img src="/img/logo-sidearea-1-1.png" alt="">
                <p class=" text-center mt-4">This is Marée, a colorful new portfolio for presenting your work. If you’re a
                    modern illustrator or a
                    designer, we made Marée for you.</p>
                <div>
                    <span class="me-3"><font-awesome-icon :icon="['fab', 'twitter']" style="color: #000000;" /></span>
                    <span class="me-3"><font-awesome-icon :icon="['fab', 'pinterest-p']" style="color: #000000;" /></span>
                    <span class="me-3"><font-awesome-icon :icon="['fab', 'facebook-f']" style="color: #000000;" /></span>
                    <span><font-awesome-icon :icon="['fab', 'linkedin-in']" style="color: #000000;" /></span>

                </div>
                <div class="input-group mt-4">
                    <input type="text" class="form-control border-0 search" placeholder="Enter your keyword..."
                        aria-label="Keyword" aria-describedby="basic-addon2">
                    <button class="input-group-text bg-transparent border-0" id="basic-addon2">
                        <font-awesome-icon :icon="['fas', 'magnifying-glass']" style="color: #f5d8ca;" />
                    </button>
                </div>
            </div>

        </div>
    </div>
</template>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;

// ...qui eventuale SCSS di AppComponent
.menu {
    min-height: 6rem;
}

.item {
    border-bottom: solid 2px transparent
}

.item:hover {
    border-bottom: solid 3px #C0E1CF;
}

.search {
    border-bottom: solid 3px #f5d8ca !important;
}

.dropdown:hover .dropdown-menu {
    display: block;
}
</style>