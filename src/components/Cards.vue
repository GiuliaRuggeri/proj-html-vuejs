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
.square {
    width: 100%;
    height: 100%;
    overflow: hidden;
}

.infocontainer {
    position: absolute;
    top: 50%;
    left: -100%;
    background-color: white;
    color: black;
    padding: 1em;
    transition: left 0.3s ease-in-out;
}

.square:hover .infocontainer {
    left: 0;
}
</style>