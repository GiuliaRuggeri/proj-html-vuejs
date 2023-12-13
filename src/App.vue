<script>
import AppNav from "./components/AppNav.vue"

import { store } from "./store.js" //state management

import PageHeader from "./components/PageHeader.vue";
import PageMain from "./components/PageMain.vue";
import PageFooter from "./components/PageFooter.vue";

export default {
	components: {
		PageHeader,
		PageMain,
		PageFooter
	},
	data() {
		return {
			store
		}
	},
	mounted() {

	},
	methods: {

	}
}
</script>

<template>
	<PageHeader />
	<PageMain />
	<PageFooter />
	<div class="stickycontainer">
		<div class="stickyred d-flex justify-content-center align-items-center">
			<img class="round" src="/svg/svg-4.svg" alt="">
		</div>
		<div class="stickywhite mt-2 d-flex justify-content-center align-items-center">
			<img class="cart" src="/svg/svg-6.svg" alt="">
		</div>
	</div>
</template>

<style lang="scss">
// importo il foglio di stile generale dell'applicazione, non-scoped
@use './styles/general.scss';
</style>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;

// ...qui eventuale SCSS di App.vue
main {
	padding: 1rem;
}

.stickycontainer {
	position: fixed;
	right: 0;
	top: 15%;
	z-index: 100;

}

.stickyred {
	background-color: crimson;
	width: 45px;
	height: 45px;
}

.stickywhite {
	background-color: white;
	width: 45px;
	height: 45px;
	box-shadow: 1px 1px 1px 1px grey;
}

.round {
	width: 30px;
}

.cart {
	width: 30px;
}
</style>