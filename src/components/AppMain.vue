<script>
export default {
    data() {
        return {
             
        };
     },
    methods: {

    }
}
</script>

<template>
    <main>
        <div class="container">
            <form>
                form 
            </form>
        </div>

        <div class="container">
            <div class="row">
                <div class="col" v-for="i in 20" :key="i">
                    yu-gi-oh card
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