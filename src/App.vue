<script>
import AppNav from "./components/AppNav.vue"

import { store } from "./store.js" //state management

import PageHeader from "./components/PageHeader.vue";
import PageMain from "./components/PageMain.vue"

export default {
	components: {
		PageHeader,
		PageMain
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
</style>