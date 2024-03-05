<script setup>

</script>

<template>
        <div class="sidebar">
            <ul class="list">
            <li class="list-item">
                <p class="item-numbers">12 765</p>
                <p class="item-text">дней мы бустим</p>
            </li>
            <li class="list-item">
                <p class="item-numbers">85 865</p>
                <p class="item-text">темных монет, заработанных нашими клиентами</p>
            </li>
            <li class="list-item">
                <p class="item-numbers">49 675</p>
                <p class="item-text">EX полученного опыта нашими клиентами</p>
            </li>
        </ul>
        </div> 
</template>

<style scoped>
.list {
    list-style: none;
    padding-top: 136px;
    padding-bottom: 136px;
    
}
.list-item {
    position: relative;
    max-width: 190px;
    
}
.list-item:nth-child(2) {
    margin: 50px 0;
}
.list-item::before{
    position: absolute;
    background-image: url('/src/assets/images/icons/information.svg');
    content: '';
    display: block;
    width: 15px;
    height: 15px;
    left: 70%;
    bottom: 100%;
}
.item-numbers {
    font-family: 'Handelson Six_CYR';
    font-size: 45px;
    font-weight: normal;
    color: var( --color-font-secondary);
}
.item-text {
    margin-top: 15px;
    font-family: 'Fira Sans';
    font-size: 18px;
    font-weight: normal;
    color: var( --color-font-secondary);
}
</style>