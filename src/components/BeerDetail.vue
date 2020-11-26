<template>
    <div v-if="beer" id="beer-detail">
        <h3>{{ beer.name }}</h3>
        <img :src="beer.image_url">
        <p>Tagline: {{beer.tagline}}</p>
        <p>Food Pairing: {{beer.food_pairing}}</p>
        <p>Description: {{beer.description}}</p>
        
        <beer-ingredients :beerIngredients="beerIngredients"></beer-ingredients>
    </div>

</template>

<script>
import BeerIngredients from './BeerIngredients.vue'
export default {
  components: { BeerIngredients },
    name: 'beer-detail',
    props: ['beer']
    


}
</script>

<style>
/* .beer-detail{
        padding:10px;
    
    
    border-radius: 10px;
    
    position: fixed;
    top:150px;
    left: 50%;
} */


</style>