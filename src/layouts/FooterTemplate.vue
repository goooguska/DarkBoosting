<script setup>
import FooterList from '@/components/FooterList.vue';

const footerList = [
    {
        title:'О компании',
        points:['Как это работает?','О нас','Отзывы','Контакты']
    },
    {
        title:'Помощь',
        points:['Гайды и лайфхаки','FAQ','Конфиденциальность','Правила и условия','Пользовательское соглашение']
    }

]
const footerListIcons=[
    {
        title:'Соцсети',
        iconsMedia:[
        '/src/assets/images/icons/discord.svg',
        '/src/assets/images/icons/facebook.svg',
        '/src/assets/images/icons/instagram.svg'
        ]
    }

]

</script>

<template>
    <footer class="footer">
        <div class="container">
            <div class="content">
                <div class="logo">
                <img src="/src/assets/images/icons/logo-white-darkBoosting.svg" alt="#">
            </div>
            <FooterList :items="footerList"/>
            <div class="lists-icons">
                <FooterList  :icons="footerListIcons"/> 
                <div class="lists-payments">
                <div class="list-payment">
                    <img src="/src/assets/images/icons/paypal-logo.png" alt="#">
                    <img src="/src/assets/images/icons/mastercard-logo.png" alt="#">
                    <img src="/src/assets/images/icons/visa-logo.png" alt="#">
                    <img src="/src/assets/images/icons/liqpay-logo.png" alt="#">

                </div>
                <div class="list-payment">
                    <img src="/src/assets/images/icons/qiwi-logo.png" alt="#">
                    <img src="/src/assets/images/icons/privat24-logo.png" alt="#">

                </div>
            </div>
            </div>
            </div>
           
            <div class="copyright">
                <p class="copyright-text">© 2016-2020 - darkboosting.com </p>
                <img class="copyright-img" src="/src/assets/images/icons/imgCopy.png" alt="#">
            </div>
        </div>
    </footer>
</template>

<style scoped>
.footer{
    background-image: url('/src/assets/images/backgrounds/footerBG.png');
    padding-top: 70px;
    display: flex;

}
.content{
    display: flex;
    justify-content: space-between;
}
.lists{
    display: flex;
}
.lists-payments{
    padding-top: 50px;
}
.list-payment{
    display: flex;
    gap: 20px;
    padding-bottom: 10px;
}
.copyright{
    display: flex;
    justify-content: space-between;
    margin-top: 55px;
}
.copyright-text{
    font-family: "Fira Sans";
    font-weight: 400;
    font-size: 16px;
    color: var(--color-font-secondary);
    opacity: 0.7;
}

</style>