<template>
  <div>
    <h1>Brewdog App</h1>
    <div class='main-container'>
      <beers-list :beers="beers"></beers-list>
      <beer-detail :beer="selectedBeer"></beer-detail>
      <button v-on:click="addFavouriteBeer(selectedBeer, selectedIngredient)">Add Favourite Beer</button>
      <favourite-beers :favouriteBeers="favouriteBeers"></favourite-beers>
      

    </div>

    </div>
</template>

<script>
import BeersList from './components/BeersList.vue';
import BeerDetail from './components/BeerDetail.vue';
import FavouriteListItem from './components/FavouriteListItem.vue';
import {eventBus} from './main.js'

export default {
  name: 'app',
  data(){
    return{
      beers: [],
      selectedBeer: null,
      favouriteBeers: []
    }
  },

  components:{
    "beers-list": BeersList,
    "beer-detail": BeerDetail,
    "favourite-beers": FavouriteListItem
  },

  mounted(){
    fetch('https://api.punkapi.com/v2/beers')
    .then(response => response.json())
    .then(data => this.beers = data)

    eventBus.$on('beer-selected', (beer) => {
      this.selectedBeer = beer
    })
  },
  methods: {
    addFavouriteBeer: function(selectedBeer) {
      if (this.favouriteBeers.includes(selectedBeer) === false) {
      this.favouriteBeers.push(this.selectedBeer)
    }
  }
  }
} 

</script>

<style>
body{
  background-color: lightblue;
  
}

</style>