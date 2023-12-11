<script>
export default {
    name: "Process",
    props: {
        dot: Object
    }
}
</script>
<template>
    <font-awesome-icon :icon="['fas', dot.icon]" size="2xl" :style="{ color: dot.iconcolor }" />
</template>
<style scoped></style>