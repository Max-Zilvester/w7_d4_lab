<template>
  <div id="favourite-beers">
    <h2>Favourite Beers</h2>
    <p v-for="beer in favouriteBeers">{{ beer.name }}</p>
  </div>
</template>

<script>
export default {
    name: 'favourite-beers',
    props: ['favouriteBeers']

}
</script>

<style>

</style>