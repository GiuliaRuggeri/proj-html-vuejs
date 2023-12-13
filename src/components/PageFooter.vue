<script>
import Articles from './Articles.vue';
import Contacts from './Contacts.vue';


export default {
    components: {
        Articles,
        Contacts,

    },
    data() {
        return {
            Articles: [
                {
                    img: "/img/h-2-blog-img-1.jpg",
                    description: "This way, loves: a detailed guide through new design",
                    author: "By Emily Fields",
                },
                {
                    img: "/img/h-2-blog-img-2.jpg",
                    description: "I try to give people a different way of looking art",
                    author: "By Emily Fields",
                },
                {
                    img: "/img/h-2-blog-img-3.jpg",
                    description: "Introduce Richard Laperrière of those amazing features",
                    author: "By Emily Fields",
                }
            ]
        }
    },


}
</script>
<template>
    <div class="container text-black text-start mt-3">
        <div class="row">
            <div class="col-4" v-for="article in Articles">
                <Articles :post="article" />
            </div>

        </div>

    </div>
    <Contacts />
</template>
<style scoped></style>