<script>
export default {
    name: "Process",
    props: {
        dot: Object
    }
}
</script>
<template>
    <!--align items center -->
    <div class="d-flex flex-column align-items-center mt-5">


        <div class="dot d-flex justify-content-center align-items-center ">
            <font-awesome-icon :icon="['fas', dot.icon]" size="2xl" :style="{ color: dot.iconcolor }" />
        </div>

        <div class="text-black text-center mt-3">
            <h5>{{ dot.title }}</h5>
            <p>{{ dot.subtitle }}</p>
        </div>
    </div>
</template>
<style scoped>
.dot {
    width: 10rem;
    height: 10rem;
    border-radius: 50%;
    background-color: #FAF7F1;
}
</style>