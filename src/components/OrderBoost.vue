<script setup>
import ButtonOutlineWhite from './UI/ButtonOutlineWhite.vue';


</script>

<template>
    <div class="content">
        <div class="container">
            <div class="sidebar">
                <h3 class="title">Играй в свое  удовольствие с помощью Darkboosting.com</h3>
                <p class="sidebar-text">Мы бустим быстро, качественно и профессионально</p>
                <ButtonOutlineWhite>Заказать буст</ButtonOutlineWhite>
            </div>
        </div>

        <div class="image">
        <img class="img-dark" src="/src/assets/images/img/Dark.png" alt="#">
        <img class="img-gamepad" src="/src/assets/images/backgrounds/gamepad.png" alt="#">

        </div>
    </div>
    
</template>

<style scoped>

.content{
    background-image: url('/src/assets/images/backgrounds/smoke-bg-order.png');
    background-repeat: no-repeat;
    display: flex;
    justify-content: space-between;
}

.sidebar{
    padding: 90px 0;
    max-width: 700px;
}
.title {
    font-family: "Handelson Six_CYR";
    font-size: 54px;
    font-weight: normal;
    color: var(--color-font-secondary);
}
.sidebar-text{
    padding-top: 10px;
    padding-bottom: 30px;
    font-family: "Fira Sans";
    font-size: 20px;
    font-weight: normal;
    color: var(--color-font-secondary);
}
.image{
    position: relative;
}
.img-dark{
    padding-top: 20px;
    position: absolute;
    right: 10%
}
.img-gamepad{
   position: absolute;
   top: 15%;
   right: 100%;
}
</style>