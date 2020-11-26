<template>
  <div id="beer_ingredients">
      <h3>Beer Ingredients</h3>
      <ul v-for="ingredient in ingredients">{{ beer.ingredient.name}}</ul>
  </div>
</template>

<script>
export default {
    name: "beer-ingredients",
    props: []

}
</script>

<style>

</style>