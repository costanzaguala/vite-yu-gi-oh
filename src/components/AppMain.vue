<script> 
import { store } from '../store.js';
import CardYugioh from './CardYugioh.vue';

export default {
    data() {
        return {
            store,
            CardYugioh,
             
        };
     },
    components: {
        CardYugioh,
    },

    methods: {

    }
}
</script>

<template>
    <main class="py-4" >
        <div class="container text-center">
            <form>
                form 
            </form>
        </div>

        <div class="container">
            <div class="row">
                <div class="col-12 col-sm-6 col-md-2" v-for="(elem, i ) in store.card" :key="i">
					<CardYugioh :card="elem"/>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>

main {
    background-color: #D48F39;
}

</style>