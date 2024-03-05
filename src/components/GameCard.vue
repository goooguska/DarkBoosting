<script setup>
defineProps({
    items: {
    type: Array,
    required: true
  },
})
</script>

<template>
        <li class="card" v-for="(item,i) of items" :key="i" 
        :style="{ 'background-image': 'url(' + item.background + ')' }" 
        style="background-repeat: no-repeat;">
            <img class="card-logo" :src="item.logo" alt="#">
            <h4 class="card-subtitle">{{ item.name }} </h4>

        </li>
</template>

<style scoped>
.card{
    width: 340px;
    display: block;
    box-shadow: 0 0 40px 5px rgba(61, 47, 80, 0.1);
    border-top-right-radius:20px;
}
.card-subtitle{
    text-align: center;
    font-size: 24px;
    font-weight: 700;
    color: var(  --color-font-primary);
    text-transform: uppercase;
    padding-bottom: 30px;
}
.card-logo{
    display: block;
    margin: 0 auto;
    padding-top:50px ;
}
.card-background{
    display: block;
   

}
</style>