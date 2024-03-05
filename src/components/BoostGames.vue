<script setup>
import GameCard from "./GameCard.vue";
import ButtonOutlineOrange from "./UI/ButtonOutlineOrange.vue";
const cardsGames = [
    {
        name: 'Valorant',
        logo:'/src/assets/images/cards/Game/Logo.png',
        background:'/src/assets/images/cards/Image/valorant1.png'
    },
    {
        name: 'WOW Classic',
        logo:'/src/assets/images/cards/Game/Logo-4.png',
        background:'/src/assets/images/cards/Image/Image-3.png'
    },
    {
        name: 'Hearthstone',
        logo:'/src/assets/images/cards/Game/Logo-6.png',
        background:'/src/assets/images/cards/Image/Image-5.png'
    },
    {
        name: 'League of Legends',
        logo:'/src/assets/images/cards/Game/Logo-2.png',
        background:'/src/assets/images/cards/Image/Image-1.png'
    },
    {
        name: 'Dota 2',
        logo:'/src/assets/images/cards/Game/Logo-1.png',
        background:'/src/assets/images/cards/Image/Image.png'
    },
    {
        name: 'Overwatch',
        logo:'/src/assets/images/cards/Game/Logo-5.png',
        background:'/src/assets/images/cards/Image/Image-4.png'
    },
    {
        name: 'CS:GO',
        logo:'/src/assets/images/cards/Game/Logo-3.png',
        background:'/src/assets/images/cards/Image/Image-2.png'
    },
    {
        name: 'WOW BFA',
        logo:'/src/assets/images/cards/Game/Logo-7.png',
        background:'/src/assets/images/cards/Image/Image-6.png'
    }   
]
</script>

<template>
    <div class="content">
        <div class="container">
                <h3 class="title">Какие  игры  мы  бустим?</h3>
                <ul class="content-list">
                    <GameCard  :items="cardsGames"/>
                </ul>
                <ButtonOutlineOrange class="button">Посмотреть каталог </ButtonOutlineOrange>
        </div>
    </div>
</template>

<style scoped>
.container{
    text-align: center;
}
.title {
    padding-top: 90px;
    font-family: "Handelson Six_CYR";
    font-size: 54px;
    font-weight: normal;
    color: var(--color-font-secondary);

}
.content{
    background-image: url('/src//assets/images/backgrounds/noize-bg.png');
    background-repeat: no-repeat;
}
.content-list{
    margin-top: 40px;
    list-style:none;
    display: flex;
    flex-flow: row wrap;
    gap: 20px;
}
.card{
    display: block;
}
.button{
    margin-top: 40px;
    display: inline-flex;
}

</style>