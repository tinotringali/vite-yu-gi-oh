<script>

import AppSearch from './AppSearch.vue';
import AppCards from './AppCards.vue';


    export default {
        name:'AppMain',
        components:{
            AppSearch,
            AppCards
        }
    }

</script>

<template>
<main>
    <AppSearch />
    <AppCards />
</main>
</template>

<style lang="scss" scoped>

</style>