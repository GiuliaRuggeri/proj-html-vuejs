<script>
export default {
    props: {
        post: Object
    }

}
</script>
<template>
    <div class="postcontainer position-relative">
        <img class="img-fluid postphoto" :src="post.img" alt="">
        <div class="mt-2">
            <h4>{{ post.description }}</h4>
            <p>{{ post.author }}</p>
        </div>

    </div>
</template>
<style scoped lang="scss">
.postphoto:hover {
    transition: 3s;
    transform: scale(1.03);
}

h4:after {
    transition: all ease-in-out .2s;
    background: none repeat scroll 0 0 #C0E1CF;
    content: "";
    display: block;
    height: 4px;
    width: 0;
}

h4:hover:after {
    width: 100%;
}
</style>