<template >
  <div class="promo">
    <div class="content">
      <div class="promo__title">
      <h1 class="title-text">
        Как получить <span class="title-span">кайф </span> от игры, если в твоей команде раки?
      </h1>
      <p class="subtitle">Закажи у нас буст и поднимись на свой реальный рейтинг</p>
      <ButtonOutline class="button"> Заказать буст</ButtonOutline>
    </div>
    <div class="promo__gift">
      <p class="gift-text">Сделай первый заказ <br> и получи дополнительно</p>
      <ul class="gift-list">
        <li class="list-item" >50 монет</li>
        <li class="list-item">ачивку</li>
        <li class="list-item">+10 EX</li>
      </ul>
    </div>
    </div>
  <img class="promo__image-raven" src="/src/assets/images/backgrounds/raven.png" alt="#">
  <img class="promo__image-grunge" src="/src/assets/images/backgrounds/grunge-background.png" alt="#">

  </div>


</template>

<script setup>
import ButtonOutline from '@/components/UI/ButtonOutline.vue'
</script>

<style scoped>

.promo {
  background-image: url('/src/assets/images/backgrounds/smoke-bg.png');
  position: relative;
}
.button{
  margin-top: 40px;
}
.promo__image-raven{
  pointer-events: none;
  position: absolute;
  top: 25%;
}
.content{
  display: flex;
  justify-content: space-between;
  margin: 0 250px;
}
.promo__title {
  padding-top: 160px;
  width: 696px;
  padding-bottom: 200px;
}

.promo__gift {
  padding-top: 270px;
  width: 301px;
  z-index: 3;
}
.promo__image-grunge{
  pointer-events: none;
  position: absolute;
  top: 20%;
  left: 68%;
}
.title-text{
  font-size: 76px;
  font-family: 'Handelson Six_CYR';
  color: var(--color-font-secondary);
  font-weight: 100;
}
.title-span{
  color: var(--color-font-highlight);

}
.subtitle{
  margin-top: 10px;
  font-size: 20px;
  color:  var( --color-font-secondary);
  font-weight: 400;
  opacity: 0.8;
 
}
.gift-text{
  text-align: right;
  font-size: 22px;
  font-weight: 400;
  color: var( --color-font-secondary);
  opacity: 0.9;
}
.gift-list{
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
  list-style: none;
}
.list-item{
  font-size: 16px;
  font-weight:500;
  color:var( --color-font-secondary);
}
.list-item::before{
  content: '';
  display: block;
  width: 60px;
  height: 60px;
}
.list-item:nth-child(1)::before{
  background-image: url('/src/assets/images/icons/coinGift.svg'); 
}
.list-item:nth-child(2)::before{
  background-image: url('/src/assets/images/icons/achieveGift.svg'); 
}
.list-item:nth-child(3)::before{
  background-image: url('/src/assets/images/icons/ratingGift.svg'); 
}
@media(max-width:1600px){
  .promo__image-raven{
    width: 100%;
    top: 35%;

  }
  .content{
    display: block;
  }
  .promo__title{
    padding-bottom: 0px;
  }
  .gift-text{
    text-align: center;

  }
  .promo__gift{
    padding: 50px 0;
   
  }
  .promo__image-grunge{
    display: none;
  }
}
</style>
