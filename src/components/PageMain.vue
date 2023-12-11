<script>
import Cards from './Cards.vue';
import Process from './Process.vue';

export default {
    name: "PageMain",
    components: {
        Cards,
        Process
    },
    data() {
        return {
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
                    icon: "lightbulb",
                    iconcolor: "",
                    title: "Then we talk about",
                    subtitle: "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself."
                },
                {
                    icon: "lightbulb",
                    iconcolor: "",
                    title: "And we think about",
                    subtitle: "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself."
                },
                {
                    icon: "lightbulb",
                    iconcolor: "",
                    title: "So we draw along",
                    subtitle: "Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself."
                }
            ]
        }
    },
}
</script>
<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-4 p-0" v-for="card in cards">
                <Cards :item="card" />
            </div>
        </div>

    </div>
    <div class="container-fluid">
        <div class="row line">
            <div class="col-3 p-0" v-for="dot in dots">
                <Process :dot="dot" />
            </div>
        </div>

    </div>
</template>
<style scoped>
.line {
    background-image: url(/img/svg-3.svg);
}
</style>