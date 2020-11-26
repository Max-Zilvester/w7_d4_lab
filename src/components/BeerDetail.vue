<template>
    <div v-if="beer" id="beer-detail">
        <h3>{{ beer.name }}</h3>
        <p>Tagline: {{beer.tagline}}</p>
        <p>Food Pairing: {{beer.food_pairing}}</p>
        <p>Description: {{beer.description}}</p>
    </div>

</template>

<script>
export default {
    name: 'beer-detail',
    props: ['beer']


}
</script>

<style>



</style>