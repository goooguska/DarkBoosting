<template>
  <header>
    <div class="container">
      <div class="info">
        <img src="@/assets/images/icons/logo.svg" alt="#" class="logo" />
        <div class="burger-menu">
          <img src="@/assets/images/icons/burger.svg" alt="#" class="burger-icon" id="burger" />
          <p class="burger-text">ИГРЫ</p>
        </div>
        <img src="@/assets/images/icons/trophyroom.svg" alt="#" class="trophy" />
      </div>
      <div class="account">
        <RouterLink to="/" class="link">ПОДАРКИ</RouterLink>
        <RouterLink to="/" class="link">МОНЕТЫ</RouterLink>
        <RouterLink to="/" class="link">КОШЕЛЁК</RouterLink>
        <DropdownList :items="profileItems" type="link">
          <img src="@/assets/images/icons/avatar-warrior.svg" alt="#" />
        </DropdownList>

        <DropdownList :items="langItems" type="lang">
          <p class="lang">РYС</p>
        </DropdownList>
      </div>
    </div>
  </header>
</template>

<script setup>
import DropdownList from '@/components/DropdownList.vue'

const profileItems = [
  {
    name: 'Профиль',
    url: '/profile'
  },
  {
    name: 'Финансы',
    url: '/finances'
  },
  {
    name: 'История заказов',
    url: '/history'
  },
  {
    name: 'Настройки',
    url: '/settings'
  },
  {
    name: 'Выйти',
    url: '/exit'
  }
]

const langItems = ['РYС', 'ENG']
</script>

<style scoped>
a {
  text-decoration: none;

  color: var(--color-font-primary);
}
ul {
  list-style: none;
}
.container {
  max-width: 1920px;
  margin: 0 auto;
  padding: 0 20px;
  justify-content: space-between;
}
.info {
  gap: 25px;
}
.burger-menu {
  gap: 8px;
}
.burger-text {
  font-size: 16px;
  font-weight: 500;
  color: var(--color-font-primary);
  font-family: 'Fira Sans';
}
.dropdown,
.burger-menu,
.info,
.container,
.link,
.dropdowns-item,
.account__dropdowns,
.account {
  display: flex;
  align-items: center;
}
.account {
  gap: 63px;
}
.lang {
  font-size: 16px;
  font-weight: 900;
  font-family: 'Fira Sans';
}
.link::before {
  content: '';
  display: inline-block;
  width: 35px;
  height: 35px;
}
.link:nth-child(1)::before {
  background-image: url('@/assets/images/icons/gift.svg');
}
.link:nth-child(2)::before {
  background-image: url('@/assets/images/icons/coin.svg');
}
.link:nth-child(3)::before {
  background-image: url('@/assets/images/icons/purse.svg');
}
.link {
  gap: 8px;
}
</style>
