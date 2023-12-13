<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Autoplay, Pagination } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';


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
            modules: [Navigation, Autoplay, Pagination],
        };
    },

    data() {
        return {

            navigation: {
                nextEl: ".swiper-button-next",
                prevEl: ".swiper-button-prev"
            },

            slides: [
                {
                    title: "Projects made with <span class='fst-italic fw-bold'>love</span>",
                    subtitle: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore. Utenim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commo.",
                    button: "Read more",
                    image: [
                        "/img/short-slider-rev-1-img-3.png"
                    ]

                },
                {
                    title: "Devotion that never <span class='fst-italic fw-bold'>ends</span>",
                    subtitle: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore.Utenim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commo.",
                    button: "Read more",
                    image: [
                        "img/h-2-slider-img-15.png", "img/h-2-slider-img-16.png"
                    ]

                }, {
                    title: "Our new folio full of <span class='fst-italic fw-bold'>joy</span>",
                    subtitle: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore. Utenim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commo.",
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
    <swiper :slides-per-view="1" :space-between="50" :navigation="navigation" @swiper="onSwiper"
        @slideChange="onSlideChange" :modules="modules" :autoplay="{
            delay: 5000,
            disableOnInteraction: false,
        }" :pagination="{
    clickable: true,

}" :loop="true" style="--swiper-pagination-color: #E1C0B0;">
        <swiper-slide v-for="slide in slides">
            <div class="container">
                <div class="row">
                    <div class="col-6 align-self-center">
                        <h1 v-html="slide.title" class="text-black title"></h1>
                        <p class="text-black">{{ slide.subtitle }}</p>
                        <button type="button" class="btn p-3">{{ slide.button }}</button>
                    </div>
                    <div class="col-6 d-flex">
                        <img v-for="img in slide.image" :src="img" alt="" class="img-fluid">
                    </div>
                </div>
            </div>
        </swiper-slide>
        <div class="swiper-button-prev">
            <div>
                <font-awesome-icon :icon="['fas', 'chevron-left']" style="color: #ffffff;" class="arrow" />
            </div>
        </div>
        <div class="swiper-button-next">
            <div>
                <font-awesome-icon :icon="['fas', 'chevron-right']" style="color: #ffffff;" class="arrow" />
            </div>
        </div>
        <div class="swiper-pagination-bullet">

        </div>

    </swiper>
</template>
<style scoped>
button {
    border-color: #F5D8CA;
}

button:hover {
    background-color: #E1C0B0;
    transition: background 0.5s ease-in-out;
}

.title {
    font-size: 5rem;
}

.swiper-button-next::after,
.swiper-button-prev::after {
    content: "";
}

.swiper-button-next,
.swiper-button-prev {

    border-radius: 50%;
    background-color: #E1C0B0;
    padding: 2rem;
}

.arrow {
    width: 20px;
    height: 20px;
}
</style>