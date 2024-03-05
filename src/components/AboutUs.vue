<script setup>

</script>

<template>
    <div class="content">
        <img class="img-about" src="/src/assets/images/backgrounds/ravensAboutUs.png" alt="">
        <div class="container">
            <div class="sidebar">
                <p class="subtitle"> Немного больше о нас</p>
                <p class="description">darkboosting.com  предоставляет профессиональные услуги по прокачке в онлайн играх.
Мы предлагаем свои услуги тем, кто не хочет напрасно расходовать свое время и нервы, самостоятельно прокачивая персонажа, развивать навыки и тратить месяцы своей жизни на получение эпических достижений. Обеспечиваем быстрый и абсолютно безопасный результат.</p>
                <p class="description">Игры увлекают и требуют много времени. Но не все игроки готовы отдавать десятки часов в неделю, для того чтобы иметь возможность опробовать высокоуровневую лигу или пробиться к вершинам рейтингов. Семья или ответственная работа могут ограничивать время, которое вы можете провести в игре, поэтому вам потребуется наша помощь, если вы хотите опробовать все возможности игры, сражаться с самыми серьезными противниками, а не топтаться месяцами внизу рейтинга или играть в низкоуровневой лиге. Наш сервис прокачки аккаунтов будет полезен тем, кто не обладает большим количеством свободного времени, но хочет опробовать все возможности своей игры.</p>
            </div>
            <img class="scroll-bar" src="/src/assets/images/img/scrollbar.png" alt="#">

          
        </div>
    </div>
    
</template>

<style scoped>
.content{
    margin-bottom: 160px;
}
.container{
    display: flex;
    justify-content: end;
}

.img-about{
    position: absolute;
}
.sidebar {
    padding-top: 170px;
    display: block;
    max-width: 761px;
}
.subtitle {
    font-family: "Fira Sans";
    font-weight: 700;
    font-size: 30px;
    text-transform: uppercase;
    color: var(--color-font-primary);

}
.description {
    font-family: "Fira Sans";
    font-weight: 400;
    font-size: 16px;
    color: var(--color-font-primary);
}
.description:nth-child(2){
    padding-top: 30px;
    padding-bottom: 10px;
}
.scroll-bar{
    margin-left: 55px;
    margin-top: 160px;
}
</style>