<template>
    
    <div>
  <li v-on:click="handleClick">{{ beer.name }}</li>
  </div>
</template>
<script>
import {eventBus} from '../main.js';



export default {
    name: 'list-item',
    props: ['beer'],
    methods: {
      handleClick() {
        eventBus.$emit('beer-selected', this.beer)
        console.log('beer', this.beer);
      }
    }
}

</script>

<style lang="css" scoped>
#list {
    display:flex;
    flex-direction: row;
    font-family: monospace;
    font-size: 20px;
    list-style-type : none;

}

</style>