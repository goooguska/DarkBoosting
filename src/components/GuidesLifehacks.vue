<script setup>
import GuidesCard from './GuidesCard.vue';
import PaginationBar from './UI/PaginationBar.vue';

const cardsGames = [
    {
        name: 'Кто являются лучшими игроками топ-лейбла League Of Legends?',
        text:'Этап розыгрыша чемпионата мира по League of Legend начнется 1 октября в Сеуле. Этот этап состоит из 12 команд',
        background:'/src/assets/images/cards/Image/guide1.png'
    },
    {
        name: 'Ведьмин лес — все карты, дата выхода и подробный гайд',
        text:'Разработчики объявили о выходе первого дополнения в году Ворона и показали шесть новых карт. Предза...',
        background:'/src/assets/images/cards/Image/guide2.png'
    },
    {
        name: 'Как не быть «вагоном» в Overwatch?',
        text:'Что делать, если реакции мангуста и крутого аима у вас нет, а побеждать в онлайн-играх очень хочется? Возможно, без «самых быстрых рук...',
        background:'/src/assets/images/cards/Image/guide3.png'
    },
    {
        name: 'Гайд по чемпионам, какие больше подойдут для начинающего игрока',
        text:'Стоит упомянуть, что в игре присутствует небольшой режим прокачки чемпионов. Всего 4 уровня...',
        background:'/src/assets/images/cards/Image/guide4.png'
    },
   
]
</script>

<template>
    <div class="container">
        <h3 class="title">Гайды  и  лайфхаки</h3>

        <ul class="content-list">
            <GuidesCard :items="cardsGames"/>
        </ul>
        <div class="more">
            <PaginationBar/>
            <RouterLink class="link" to="/guides">
                <img class="img" src="/src/assets/images/icons/eye-orange-more.svg" alt="#"> 
                Посмотреть все гайды</RouterLink>
        </div>

        
         
    </div>
</template>

<style scoped>

.title {
    margin-top: 120px;
    text-align: center;
    font-family: "Handelson Six_CYR";
    font-size: 54px;
    font-weight: normal;
    color: var(--color-font-primary);
}
.content-list{
    margin-top: 40px;
    list-style:none;
    display: flex;
    flex-flow: row wrap;
    gap: 20px;
}
.more{
    display: flex;
    align-items: center;
    margin-top: 35px;
    margin-bottom: 95px;
}
.link{
    margin-left: 145px;
    display: flex;
    align-items: center;
    color: var(--color-font-third);
    font-size: 15px;
}
.img{
    margin-right: 10px;
}
</style>