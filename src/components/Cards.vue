<script>
export default {
    name: "Cards",
    props: {
        item: Object,
    }
}
</script>
<template>
    <div class="position-relative square">
        <img class="img-fluid" :src="item.image" alt="">
        <div class="position-absolute top-50 bg-white text-black p-3 infocontainer">
            <h3>{{ item.title }}</h3>
            <p>{{ item.subtitle }}</p>
        </div>
    </div>
</template>
<style scoped>
.infocontainer {
    display: none;

}

.square:hover .infocontainer {
    display: block;


    /* animation: MyDiv;
    animation-duration: 1s;
    animation-iteration-count: 2;
    animation-timing-function: ease-in;
    animation-direction: normal;
}

@keyframes MyDiv {
    0% {
        left: 0px;
        top: 0px;
    }

    100% {
        left: 0px;
        top: 0px;
    } */
}
</style>