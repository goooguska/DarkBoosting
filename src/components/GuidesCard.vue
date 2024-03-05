<script setup>
defineProps({
    items: {
    type: Array,
    required: true
  },
})
</script>

<template>
        <li class="card" v-for="(item,i) of items" :key="i" >
            <img :src="item.background" alt="@">
            <div class="card-description">
                <h4 class="card-subtitle">{{ item.name }} </h4>
                <p class="card-text">{{ item.text }}</p> 
            </div>
            <div class="more">
                <RouterLink class="link" to="/more" >Подробнее <img class="arrow" src="/src/assets/images/icons/arrow-more-right.svg" alt="#"> </RouterLink>

            </div>
        </li>
</template>

<style scoped>
.card{
    width: 340px;
    display: block;
    box-shadow: 0 0 40px 5px rgba(61, 47, 80, 0.1);
    border-top-right-radius:20px;
}
.card-description{
    padding: 30px 20px;
    max-width: 316px;
}
.card-subtitle{
    font-size: 18px;
    font-weight: 700;
    color: var(  --color-font-primary);
    text-transform: uppercase;
}
.card-text{
    padding-top: 10px;
    font-size: 15px;
    font-weight: 400;
    color: var(  --color-font-primary);
    padding-bottom: 30px;
}
.more{
    background-image: url('/src/assets/images/backgrounds/cardBG.png');
    text-align: right;
 
}
.link{
    padding: 18px 30px;
    display: flex;
    align-items: center;
    justify-content: end;

}
.arrow{
    margin-left: 5px;
}
.link:hover{
    transition: 0.3s ease-in-out;
    color: #9562BD;
    
}
</style>