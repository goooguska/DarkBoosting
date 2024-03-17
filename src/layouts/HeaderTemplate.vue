<script setup>
import BurgerMenu from '@/components/BurgerMenu.vue'
import DropdownList from '@/components/DropdownList.vue'
const gameItems = [
  {
    name: 'League of Legends',
    url: '/LeagueOfLegends'
  },
  {
    name: 'WOWClassic',
    url: '/WoWClassic'
  },
  {
    name: 'Hearthstone',
    url: '/Hearthstone'
  },
  {
    name: 'Valorant',
    url: '/Valorant'
  },
  {
    name: 'Dota2',
    url: '/Dota2'
  },
  {
    name: 'Overwatch',
    url: '/Overwatch'
  },
  {
    name: 'CSGO',
    url: '/CSGO'
  },
  {
    name: 'WOWBFA',
    url: '/WOWBFA'
  }
]
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
<template>
  <header>
    <div class="container">
      <div class="info">
        <img src="@/assets/images/icons/logo.svg" alt="#" class="logo" />

        <BurgerMenu :items="gameItems" type="game">
          <p class="text">ИГРЫ</p>
        </BurgerMenu>

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
  cursor: pointer;
  gap: 8px;
}
.text {
  font-size: 16px;
  font-weight: 500;
  color: var(--color-font-primary);
  font-family: 'Fira Sans';
}

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
  cursor: pointer;
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
.lang:hover,
.link:hover {
  color: var(--color-font-third);
  transition: 0.3s ease-in-out;
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
  font-weight: 500;
  gap: 8px;
}
</style>
