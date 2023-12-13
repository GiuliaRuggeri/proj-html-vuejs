<script>
import Cards from './Cards.vue';
import Process from './Process.vue';
import Work from './Work.vue';
import { store } from '../store';


export default {
    name: "PageMain",
    components: {
        Cards,
        Process,
        Work,

    },
    data() {
        return {

            store,

            cards: [
                {
                    image: "/img/h-2-port-img-1.jpg",
                    title: "All these illustrations",
                    subtitle: "Illustration",
                },
                {
                    image: "/img/h-2-port-img-2.jpg",
                    title: "Type and illustrations",
                    subtitle: "Illustration",
                },
                {
                    image: "/img/h-2-port-img-3.jpg",
                    title: "Draw and illustrate",
                    subtitle: "Illustration",
                },
                {
                    image: "/img/h-2-port-img-4.jpg",
                    title: "Illustrations of novels",
                    subtitle: "Illustration",
                },
                {
                    image: "/img/h-2-port-img-5.jpg",
                    title: "Too many illustrations",
                    subtitle: "Illustration",
                },
                {
                    image: "/img/h-2-port-img-6.jpg",
                    title: "Dreams are illustrations",
                    subtitle: "Illustration",
                }
            ],
            dots: [
                {
                    icon: "lightbulb",
                    iconcolor: "#badac9",
                    title: "First there's an idea",
                    subtitle: "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself."
                },
                {
                    icon: "comment",
                    iconcolor: "#f8d12d",
                    title: "Then we talk about",
                    subtitle: "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself."
                },
                {
                    icon: "cloud",
                    iconcolor: "#80465f",
                    title: "And we think about",
                    subtitle: "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself."
                },
                {
                    icon: "pen-ruler",
                    iconcolor: "#eb6950",
                    title: "So we draw along",
                    subtitle: "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself."
                }
            ]
        }
    },
}
</script>
<template>
    <div class="position-relative">
        <div class="container-fluid">
            <div class="row">
                <div class="col-4 p-0" v-for="card in cards">
                    <Cards :item="card" />
                </div>
            </div>

        </div>
        <div class="dotwrapper">
            <div class="row line">
                <div class="col-3 d-flex  justify-content-center" v-for="dot in dots">
                    <Process :dot="dot" />
                </div>
            </div>

        </div>
        <Work />
        <a href="#" class="stickyarrow d-flex justify-content-center align-items-center">
            <img class="arrow" src="/svg/svg-2.svg" alt="">
        </a>



    </div>
</template>
<style scoped lang="scss">
.line {
    background-image: url(/svg/svg-3.svg);
    background-position: center;
    background-repeat: no-repeat;
    padding: 3rem
}

.dotwrapper {
    min-height: 20rem;
}

.stickyarrow {
    position: fixed;
    background-color: #D8F0E3;
    right: 0;
    bottom: 15%;
    z-index: 100;
    width: 60px;
    height: 60px;
    scroll-behavior: smooth;

}
</style>