<script>
import axios from 'axios';

    export default {
        name:'AppCards',
        data(){
            return{
                cardsYu:[]
            }
        },
        created(){
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
            .then((response) => {
                console.log(response)
                this.cardsYu = response.data.data;
            })
        }
        
    }
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-2" v-for="cards in cardsYu">
                carta
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
div{
    background-color: white;
}
</style>