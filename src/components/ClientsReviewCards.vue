<script setup>
import PaginationBar from './UI/PaginationBar.vue';


</script>

<template>
    <div class="reviews">
        <h3 class="title">Что  клиенты  говорят  о  нас?</h3>
        <p class="text">Также читай отзывы на <RouterLink  class="text-strong" to="/servis"> форумах </RouterLink>
             и <RouterLink  class="text-strong" to="/servis"> сервисе отзывов</RouterLink> </p>
             <div class="images">
                <img  src="/src/assets/images/img/Review.png" alt="#">
                <img  src="/src/assets/images/img/Review2.png" alt="#">
                <img class="review-img"  src="/src/assets/images/img/Review1.png" alt="#">
             </div>
             <PaginationBar class="pagination"/>

        

    </div>
</template>

<style scoped>
.pagination{
    margin-top: 120px;
    margin-bottom: 90px;
}
.images{
    position: relative;
    
}

.review-img{
    position: absolute;
    z-index: 5;
    top: 34%;
    left: 29%;
}
.reviews{
    text-align: center;
}
.title {
    position: relative;
    padding-top: 115px;
    padding-bottom: 10px;
    font-family: "Handelson Six_CYR";
    font-size: 54px;
    font-weight: normal;
    color: var(--color-font-primary);
}
.title::before{
    position: absolute;
    background-image: url('/src/assets/images/icons/informationBlack.svg');
    content: '';
    display: block;
    width: 20px;
    height: 20px;
    left: 82%;
    top: 55%;
}
.text {
    font-family: "Fira Sans";
    font-size: 20px;
    font-weight: normal;
    color: var(--color-font-primary);
}
.text-strong {
    color: var(--color-font-primary);
    font-weight:700;
    text-decoration: underline;
}
</style>