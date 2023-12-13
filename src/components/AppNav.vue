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
                        [
                            {
                                title: "Main home"
                            },
                            {
                                title: "Prova"
                            },
                            {
                                title: "Prova"
                            }
                        ],

                    ]

                },
                {
                    title: "Pages",
                    submenu: [
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ]

                    ]
                },
                {
                    title: "Portfolio",
                    submenu: [
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ],
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ],
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ],
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ]


                    ]

                },
                {
                    title: "Blog",
                    submenu: [
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ]

                    ]


                },
                {
                    title: "Shop",
                    submenu: [
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ]
                    ]
                },
                {
                    title: "Elements",
                    submenu: [
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ],
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ],
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ],
                        [
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            },
                            {
                                title: "prova"
                            }
                        ],


                    ]
                }

            ]
        }
    },
}



</script>

<template>
    <nav class="navbar bg-white align-items-center menu">
        <div class="container-fluid">
            <img src="img/logo-sidearea-1.png" alt="">
            <div class="d-flex text-black">

                <div class="nav-item dropdown position-static" v-for="item in menuItems" :key="item.title">

                    <span class="me-4 item" type="button" aria-expanded="false">
                        {{ item.title }}
                    </span>


                    <div class="dropdown-menu" v-if="item.submenu"
                        :class="[item.submenu && item.submenu.length > 1 ? 'dropdown-menu-right' : '']">
                        <div class="d-flex">
                            <div v-for="submenu in item.submenu" class="flex-fill text-center">
                                <ul class="list-unstyled">
                                    <li v-for="subitem in submenu" class="dropdown-item bg-transparent">
                                        {{ subitem.title }}
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>

                </div>

                <img data-bs-toggle="offcanvas" data-bs-target="#offcanvasScrolling" src="/svg/svg-1.svg" alt="">
            </div>
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

    background-color: #FAF7F1;
}

.dropdown-menu-right {
    right: 0 !important;
    left: auto !important;
    width: 100%;

}

li {
    border-bottom: solid 2px transparent;
}

li:hover {
    border-bottom: solid 2px #C0E1CF;
}
</style>