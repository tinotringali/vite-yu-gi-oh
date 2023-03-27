<script>
import AppCardsYuGiOh from './AppCardsYuGiOh.vue';
import axios from 'axios';



    export default {
        name:'AppCards',
        components:{
            AppCardsYuGiOh
        },

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
    <div class="container p-5">
        <div class="row ">
            <div class="foundCards">
                <div>
                    Found 30 cards
                </div>
            </div>
            <div class="col-12 col-sm-2" v-for="cards in cardsYu.slice(0, 30)">
                <AppCardsYuGiOh :img="cards.card_images[0].image_url" :title="cards.name" :type="cards.archetype"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
div{
    background-color: white;
}

.foundCards {
        
    color: white;
    padding: 0 25px;
    div{
        background-color:#212529;
        padding: 30px 30px;
        
    }
}
</style>