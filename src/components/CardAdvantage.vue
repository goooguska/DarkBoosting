<template>
    <div class="card"  v-for="(card,i) of cards" :key="i">
        <img class="card-image"   :src="`${card.image}`" alt="#" >
        <h4 class="card-subtitle" >{{ card.title }}</h4>
        <p class="card-text" >{{ card.description }} </p>        
    </div>
</template>

<script setup>
import { defineProps } from 'vue'
defineProps({
  cards: {
    type: Array,
    required: true
  },
 
})
</script>

<style scoped>
.card{
    max-width: 310px;
}
.card-subtitle{
    font-size: 24px;
    font-weight: 700;
    color: var(  --color-font-primary);
    text-transform: uppercase;
    padding: 10px 0;
}
.card-text{
    font-size: 16px;
    font-weight: 400;
    color: var(  --color-font-primary);

}

</style>