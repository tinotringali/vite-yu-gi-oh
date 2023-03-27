<script>
    export default {
        name:'AppCardsYuGiOh',
        props:{
            img: String,
            title: String,
            type: String
        }
    }
</script>

<template>
<article class="text-center">
    <div class="img"><img :src="img" alt=""></div>
    <h4>{{ title }}</h4>
    <p>{{ type }}</p>
</article>
</template>

<style lang="scss" scoped>
img{
    width: 100%;
}
</style>