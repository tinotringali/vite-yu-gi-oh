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
<article class="text-center mb-3">
    <div class="img"><img :src="img" alt=""></div>
    <div class="infoCards">
        <h5 class="fs-5 text-light py-2 text">{{ title }}</h5>
        <p>{{ type }}</p>
    </div>
</article>
</template>

<style lang="scss" scoped>
img{
    width: 100%;
}

.infoCards{
    background-color: #d48f38;
    height: 120px;
}

</style>