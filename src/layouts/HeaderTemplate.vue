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
        <DropdownList />
        <!-- <div class="account__dropdowns">
          <div
            class="dropdown"
            id="profile"
            v-on:mouseenter="openProfile = true"
            v-on:mouseleave="openProfile = false"
          >
            <img src="@/assets/images/icons/avatar-warrior.svg" alt="#" />
            <img src="@/assets/images/icons/arrow-down.svg" alt="#" />
          </div>

          <div class="dropdown__list" v-if="openProfile === true">
            <ul class="list-items" id="profileList ">
              <li class="list-items-item" v-for="item of profileItems" v-bind:key="item">
                <RouterLink class="list-items-item-link" to="">{{ item }} </RouterLink>
              </li>
            </ul>
          </div>

          <div
            class="dropdown"
            id="lang"
            v-on:mouseenter="openLang = true"
            v-on:mouseleave="openLang = false"
          >
            <p class="lang">РYС</p>
            <img src="@/assets/images/icons/arrow-down.svg" alt="#" />
          </div>

          <div class="dropdown__list" v-if="openLang === true">
            <ul class="list-items" id="langList ">
              <li class="list-items-item" v-for="item of langItems" v-bind:key="item">
                <RouterLink class="list-items-item-link" to="">{{ item }} </RouterLink>
              </li>
            </ul>
          </div>
        </div> -->
      </div>
    </div>
  </header>
</template>

<script setup>
import DropdownList from '@/components/DropdownList.vue'

// const openProfile = ref(false)
// const openLang = ref(false)

// const profileItems = ['Профиль', 'Финансы', 'История заказов', 'Настройки', 'Выйти']
// const langItems = ['РYС', 'ENG']
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
.account__dropdowns {
  position: relative;

  gap: 34px;
}
.dropdown {
  gap: 4px;
  cursor: pointer;
}

.list-items {
  text-align: center;
  position: absolute;
  left: 40%;
}

.lang {
  font-size: 16px;
  font-weight: 700;
  color: var(--color-font-primary);
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
