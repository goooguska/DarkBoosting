<template>
<div class="content">
    <div class="container">
            <h3 class="title">Получи  гарантированную  награду</h3>
            <p class="description"> Мы заботимся про наших клиентов, поэтому заказывая буст у нас, ты можешь получить различные награды</p>
            <GuarantRewardList :items="cards"></GuarantRewardList>
            <ButtonOutlineWhite>Заказать буст</ButtonOutlineWhite>
    </div>
</div>

</template>

<script setup>
import GuarantRewardList from "./GuarantRewardList.vue";
import ButtonOutlineWhite from "./UI/ButtonOutlineWhite.vue";
const cards = [
    {
        name:'темные монеты',
        url:'/src/assets/images/icons/coinGarant.svg'
    },
    {
        name:'+баллы в EX',
        url:'/src/assets/images/icons/ratingGarant.svg'
    },
    {
        name:'ачивки',
        url:'/src/assets/images/icons/achieveGarant.svg'
    },
    {
        name:'ранги',
        url:'/src/assets/images/icons/rank.svg'
    },
    {
        name:'расширение кошелька',
        url:'/src/assets/images/icons/purseGarant.svg'
    },
    {
        name:'+% к кешбеку',
        url:'/src/assets/images/icons/cashback.svg'
    },
    {
        name:'+скидка на заказ',
        url:'/src/assets/images/icons/discountGarant.svg'
    }
]
</script>

<style scoped>
.content {
    background-image: url('/src/assets/images/backgrounds/giftsGuarantBG.png');

}
.container {

    max-width: 1420px;
    width: 100%;
    margin: 0 auto;
}

.title {
    font-family: "Handelson Six_CYR";
    font-size: 54px;
    font-weight: normal;

}
.description {
}
</style>