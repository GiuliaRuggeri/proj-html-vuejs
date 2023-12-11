<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';

export default {
    name: "Slider",
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        return {
            onSwiper,
            onSlideChange,
            modules: [Navigation],
        };
    },

    data() {
        return {
            slides: [
                {
                    title: "Projects made with love",
                    subtitle: "lorem ipsum",
                    button: "Read more",
                    image: [
                        "/img/short-slider-rev-1-img-3.png"
                    ]

                },
                {
                    title: "Devotion that never ends",
                    subtitle: "lorem ipsum",
                    button: "Read more",
                    image: [
                        "img/h-2-slider-img-15.png", "img/h-2-slider-img-16.png"
                    ]

                }, {
                    title: "Our new folio full of joy",
                    subtitle: "Lorem ipsum",
                    button: "Read more",
                    image: [
                        "img/h-2-slider-img-11.png"
                    ]

                },
            ]
        }
    },
}
</script>
<template>
    <swiper :slides-per-view="1" :space-between="50" navigation @swiper="onSwiper" @slideChange="onSlideChange"
        :modules="modules">
        <swiper-slide v-for="slide in slides">
            <div class="container">
                <div class="row">
                    <div class="col-6 align-self-center">
                        <h1 class="text-black">{{ slide.title }}</h1>
                        <p class="text-black">{{ slide.subtitle }}</p>
                        <button type="button" class="btn">{{ slide.button }}</button>
                    </div>
                    <div class="col-6 d-flex">
                        <img v-for="img in slide.image" :src="img" alt="">
                    </div>
                </div>
            </div>
        </swiper-slide>

    </swiper>
</template>
<style scoped>
button {
    border-color: #F5D8CA;
}
</style>