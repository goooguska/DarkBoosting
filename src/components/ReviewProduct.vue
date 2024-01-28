<template>

    <div class="container">

        <div class="review">
            <img class="review-raven" src="/src/assets/images/backgrounds/flying-raven-2.png" alt="#">

            <div class="review__title">
                <img src="/src/assets/images/backgrounds/Go-to-the-dark-side.png" alt="#">
            </div>
            <div class="review__info">
                <h3 class="info-subtitle">Нам  важна  наша  репутация! Читай  отзывы  на:</h3>
                <ul class="info-list">
                    <li class="list-item"><RouterLink to="/forum"  class="link">Форумах </RouterLink></li>
                    <li class="list-item"><RouterLink to="/servisReview" class="link">Сервисе отзывов </RouterLink></li>
                    <li class="list-item"><RouterLink to="/website" class="link">Нашем сайте </RouterLink></li>

                </ul>
            </div>    

        </div>
    </div>
    
</template>

<script setup>

</script>

<style scoped>
ul{
    list-style: none;
}
a{
    text-decoration: none;
}
.container {
    max-width: 1920px;
  margin: 0 auto;
  padding: 0 20px;
  background-image: url('/src/assets/images/backgrounds/smoke-bg-2.png');


}
.review {
    display: flex;
    gap: 412px;
    padding-top: 90px;
    position: relative;
}

.review__info {
    z-index: 3;
    width: 100%;
    max-width: 693px;
}
.info-subtitle {
    font-size: 54px;
    font-family: "Handelson Six_CYR";
    font-weight: 100;
    color: var(--color-font-secondary);
}
.info-list {
    display: flex;
    gap: 33px;
    margin-top: 42px;
}
.link{
    color: var(--color-font-secondary);
    font-weight: 700;
    font-size: 18px;
    padding-left: 8px;
}
.list-item::before{
    display: inline-block;
    content: '';
    width: 30px;
    height: 30px;
}
.list-item:nth-child(1)::before{
    background-image: url('/src/assets/images/icons/speech-cloud.svg');
}
.list-item:nth-child(2)::before{
    background-image: url('/src/assets/images/icons/like.svg');
}
.list-item:nth-child(3)::before{
    background-image: url('/src/assets/images/icons/logo-tiny.svg');
}
.list-item {
    display: flex;
    align-items: center;
    padding: 20px 23px;
    border-radius: 0px 30px;
    background: var(--color-background-button)
}
.review-raven{
    position: absolute;
    bottom: 15%;
    right: 45%;
    background-image: url('/src/assets/images/backgrounds/flying-raven-2.png');

}
@media(max-width:1600px){
    .review{
        justify-content: space-between;
        gap: 0;

    }
}
</style>