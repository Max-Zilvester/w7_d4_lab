<template>
    <div v-if="beer" id="beer-detail">
        <h3>{{ beer.name }}</h3>
        <img :src="beer.image_url">
        <p>Tagline: {{beer.tagline}}</p>
        <p>Food Pairing: {{beer.food_pairing}}</p>
        <p>Description: {{beer.description}}</p>
        
        <beer-ingredients :beerIngredients="beerIngredients"></beer-ingredients>
        <p>{{ beer.ingredients.malt[0, 1] }}</p>
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
.beer-detail{
    width:50%;

}


</style>