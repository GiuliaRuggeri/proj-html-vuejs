<script>
import Cards from './Cards.vue';

export default {
    name: "PageMain",
    components: {
        Cards,
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
</template>
<style scoped></style>