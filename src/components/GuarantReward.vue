<template>
<div class="content">
    <div class="container">
            <h3 class="title">Получи  гарантированную  награду</h3>
            <p class="description"> Мы заботимся про наших клиентов, поэтому заказывая буст у нас, ты можешь получить различные награды</p>
            <GuarantRewardList :items="cards"></GuarantRewardList>
            <ButtonOutlineWhite class="button">Заказать буст</ButtonOutlineWhite>
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
    margin-top: 140px;
    background-image: url('/src/assets/images/backgrounds/giftsGuarantBG.png');

}
.container {
    text-align: center;
    max-width: 1420px;
    width: 100%;
    margin: 0 auto;
}

.title {
    padding-top: 90px;
    font-family: "Handelson Six_CYR";
    font-size: 54px;
    font-weight: normal;
    color: var(--color-font-secondary);

}
.description {
    font-family: 'Fira Sans';
    font-size: 20px;
    font-weight: normal;
    color: var(--color-font-secondary);
    opacity: 0.8;
    margin-bottom: 30px;
}
.button{
    margin-top: 40px;
}
</style>