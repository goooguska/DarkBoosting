<template>
    <div class="container">
      
        <div class="content">
            <div class="image">
            <img src="/src/assets/images/img/example-2.png" alt="#">
        </div>
            <div class="description">
            <h3 class="title">Гибкий  калькулятор  поможет  точно  расчитать  цену  за  пару  кликов </h3>
            <p class="text">Равным образом дальнейшее развитие различных форм деятельности обеспечивает широкому кругу (специалистов) участие в формировании существенных финансовых
                 и административных условий. Задача организации, в особенности же сложившаяся структура организации влечет за собой процесс внедрения и модернизации существенных
                 финансовых и административных условий.</p>
                <div class="buttons">
                    <ButtonFilled>Попробовать</ButtonFilled>
                    <ButtonOutlinedOrange>Смотреть видео</ButtonOutlinedOrange>
                </div>
           
        </div>
      
        </div>
        
        
    </div>
</template>

<script setup>
import ButtonOutlinedOrange from "./UI/ButtonOutlineOrange.vue";
import ButtonFilled from "./UI/ButtonFilled.vue";

</script>

<style scoped>
.container{
    max-width: 1420px;
    width: 100%;
    margin: 0 auto;
}
.content{
    margin-top: 140px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.description {
    max-width: 610px;
}
.title {
    font-family: "Handelson Six_CYR";
    font-weight: 100;
    font-size: 54px;
    color: var(--color-font-primary);
}
.text {
    font-family: "Fira Sans";
    font-weight:400;
    font-size: 20px;
    color: var(--color-font-primary);
    margin-top: 20px;
    margin-bottom: 30px;

}
.buttons{
   display: flex;
   gap: 36px;
   align-items: center;
  
}
</style>