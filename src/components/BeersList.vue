<template>
<div>
  <list-item v-for="(beer, index) in beers" :beer="beer" :key="index"></list-item>
</div>
</template>


<script>
import ListItem from './ListItem.vue'

export default {
    name: 'beers-list',
    props: ['beers'],
    components: {
        "list-item": ListItem
    }


}
</script>

<style lang="css" scoped>
div{
    display:flex;
    flex-direction: column;
}

</style>