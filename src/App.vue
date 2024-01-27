<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios  from 'axios';
import { store } from './store';

export default {
    data() {
        return {
            store
             
        };
     },

    components: {
        AppHeader,
        AppMain,
        AppFooter
    },

    methods: {

    },
   created () {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
            this.store.card = response.data.data
            console.log(this.store.card)
            });
    }
}
</script>

<template>

    <AppHeader/>

    <AppMain/>

    <AppFooter/>

</template>

<style lang="scss">
    @use "assets/scss/main.scss" as *;
    @use "assets/scss/partials/reset.scss" as *;
</style>
