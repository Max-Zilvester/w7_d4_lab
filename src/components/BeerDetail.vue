<template>
    <div v-if="beer" id="beer-detail">
        <h3>{{ beer.name }}</h3>
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



</style>