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
}
</style>