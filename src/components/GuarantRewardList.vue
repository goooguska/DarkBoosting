<template>
    <div>
        <ul class="list">
                <li class="list-item"
                v-for="(item, i) of items" :key="i" > 
                <img class="img" :src='item.url' alt="#">   
                {{ item.name }}  
                </li>
            </ul>
    </div>
</template>

<script setup>
defineProps({
  items: {
    type: Array,
    required: true
  }
  
})
</script>

<style scoped>
.list {
    list-style: none;
    display: flex;
    justify-content: space-between;
    gap: 15px;
}
.img{
    margin: 0 auto;
    display: block;
    
}
.list-item {
   
    position: relative;
    text-align: center;
    min-width: 190px;
    border-radius: 0px 30px;
    background:var(--color-card-background);
    font-family: 'Fira Sans';
    font-size: 20px;
    font-weight: normal;
    color: var( --color-font-secondary);
    padding: 20px 25px;
}
.list-item::before{
    position: absolute;
    background-image: url('/src/assets/images/icons/information.svg');
    content: '';
    display: block;
    width: 15px;
    height: 15px;
    top: 5%;
    left: 5%;
}
</style>