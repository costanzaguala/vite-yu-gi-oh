<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios  from 'axios';


export default {
    data() {
        return {
             
        };
     },

    components: {
        AppHeader,
        AppMain,
        AppFooter
    },

    methods: {

    },
    mounted () {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
        .then((response) => {
            console.log (response)
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
    @import "assets/scss/partials/reset.scss";
</style>
