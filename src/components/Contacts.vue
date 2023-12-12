<script>
export default {
    name: "Contacts",


}
</script>
<template>
    <div class="wrapper">
        <div class="container text-black p-4">
            <div class="row">
                <div class="col-3 contacts">
                    <img src="/img/logo-sidearea-1.png" alt="">
                    <p>Let's get creative</p>
                </div>
                <div class="col-3 contacts">
                    <p>maree@qodeinteractive.com</p>
                    <p>+44645 321 789</p>
                </div>
                <div class="col-3 contacts">
                    <p>Avenue d’Auderghem 10</p>
                    <p>1040 Brussels, Belgium</p>
                </div>
                <div class="col-3 contacts">
                    <p>Stay in touch with us</p>

                    <span class="me-3"><font-awesome-icon :icon="['fab', 'twitter']" /></span>
                    <span class="me-3"><font-awesome-icon :icon="['fab', 'pinterest-p']" /></span>
                    <span class="me-3"><font-awesome-icon :icon="['fab', 'facebook-f']" /></span>
                    <span><font-awesome-icon :icon="['fab', 'linkedin-in']" /></span>


                </div>
            </div>

        </div>
    </div>
</template>
<style scoped>
.wrapper {
    background-color: #C0E1CF;
}

.contacts>p:after {
    transition: all ease-in-out .2s;
    background: none repeat scroll 0 0 #F5D8CA;
    content: "";
    display: block;
    height: 4px;
    width: 0;
}

.contacts>p:hover:after {
    width: 70%;
}

span:hover {
    color: white !important;
}
</style>