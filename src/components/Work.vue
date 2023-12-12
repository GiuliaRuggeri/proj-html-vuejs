<script>
export default {
    name: "Work"
}
</script>
<template>
    <div class="container-fluid text-center text-black work">
        <h1>Want to work with us? Send us a message!</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore. Ut
            enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commo.</p>
        <button type="button" class="btn secondbutton p-3">CONTACT</button>
    </div>
</template>
<style scoped>
.work {
    background-image: url(/img/h-2-background-1.jpg);
    min-height: 20rem;
    padding: 10rem
}

.secondbutton {
    background-color: #D8F0E3;
}

.secondbutton:hover {
    background-color: #E1C0B0;
    color: white;
    transition: background 0.5s ease-in-out;
}
</style>