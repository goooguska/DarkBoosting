<template>
    <div class="advantages">
        <CardAdvantage :cards="cardItems"/>
    </div>
</template>

<script setup>
import CardAdvantage from "@/components/CardAdvantage.vue";
const cardItems =[{
        image:'/src/assets/images/icons/discount.svg',
        title:'Уникальная система поощрений',
        description:'Регистрируйся на сайте, делай заказы, выполняй задания и получай даркмонети, скидки, ачивки. Продвигайся по уровню и получай дополнительные награды.'
    },
    {
        image:'/src/assets/images/icons/protect.svg',
        title:'впн протекция на каждый заказ',
        description:'Система впн скрывает IP бустера, что делает буст необноружимым. '
    },
    {
        image:'/src/assets/images/icons/offline.svg',
        title:'Конфиденциальность и офлайн режим',
        description:'Все услуги на нашем сайте конфиденциальны, также во всех играх, бустер играет только в офлайн режиме, скрывая факт нахождения его от друзей.'
    },
    {
        image:'/src/assets/images/icons/time-warranty.svg',
        title:'Гарантия времени',
        description:'Каждый заказ сдается точно в срок, или мы вернем вам деньги.'
    }]
</script>

<style scoped>
.advantages{
    display: flex;
    justify-content: center;
    margin-top: 200px;
    gap: 60px;
}

</style>