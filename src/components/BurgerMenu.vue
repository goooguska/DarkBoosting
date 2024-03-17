<script setup>
import { defineProps, ref } from 'vue'
let show = ref(false)
let dropdownShow = ref(false)

function toggleBurger() {
  show.value = !show.value
}
defineProps({
  items: {
    type: Array,
    required: true
  },
  type: {
    type: String,
    required: true,
    default: 'game'
  }
})
const categories = [
  {
    name: 'Прокачка дивизионов',
    url: '/divisions'
  },
  {
    name: 'Квалифицированные игры',
    url: '/qualifications'
  },
  {
    name: 'Дуо игры',
    url: '/duo'
  },
  {
    name: 'Точные победы',
    url: '/wins'
  },
  {
    name: 'Победы в нормалах',
    url: '/normalWins'
  },
  {
    name: 'Обучение',
    url: '/tutorial'
  },
  {
    name: 'Мастерство чемпионов',
    url: '/champions'
  }
]
</script>
<template>
  <slot />
  <div class="burger-menu">
    <img
      src="@/assets/images/icons/burger.svg"
      alt="#"
      class="burger-icon"
      id="burger"
      @click="toggleBurger()"
    />
    <transition name="list">
      <ul class="burger-list" v-if="show === true">
        <li class="list-item" v-for="(item, i) of items" :key="i" @mouseenter="dropdownShow = true">
          <RouterLink class="link" :to="item.url">{{ item.name }} </RouterLink>
        </li>
      </ul>
    </transition>
    <ul class="dropdown" v-show="dropdownShow" @mouseleave="dropdownShow = false">
      <li class="dropdown-item" v-for="(category, i) in categories" :key="i">
        <RouterLink class="link-dropdown" :to="category.url">{{ category.name }} </RouterLink>
      </li>
    </ul>
  </div>
</template>
<style scoped>
ul {
  list-style: none;
}
a {
  text-decoration: none;
  color: var(--color-font-primary);
  font-weight: 400;
  font-size: 16px;
}
.dropdown {
  position: absolute;
  top: -80%;
  left: 250%;
  z-index: 5;
  background: var(--color-font-secondary);
  background-image: url('/src/assets/images/backgrounds/burgerBG.png');
}
.dropdown-item {
  width: 270px;
  padding: 15px 20px;
}
.dropdown-item:hover {
  background: radial-gradient(50% 50% at 50% 50%, rgba(255, 255, 255, 0) 0%, #a1a1a1 100%), #e6e6e6;
}
.dropdown-item:nth-child(1) {
  margin-top: 80px;
}
.link-dropdown {
}

.list-enter-active,
.list-leave-active {
  transition: opacity 0.5s ease;
}

.list-enter-from,
.list-leave-to {
  opacity: 0;
}
.burger-menu {
  position: relative;
}
.burger-list {
  background: var(--color-font-secondary);
  position: absolute;
  z-index: 5;
  top: -100%;
  right: -150%;
  background-image: url('/src/assets/images/backgrounds/burgerBG.png');
}
.list-item {
  padding: 15px 20px;
  display: flex;
  align-items: center;
  position: relative;
}
.list-item:hover {
  background: radial-gradient(50% 50% at 50% 50%, rgba(255, 255, 255, 0) 0%, #a1a1a1 100%), #e6e6e6;
}

.list-item::before {
  content: '';
  display: inline-block;
  width: 50px;
  height: 50px;
  margin-right: 10px;
}
.list-item::after {
  background-image: url('/src/assets/images/icons/arrow-right.svg');
  background-repeat: no-repeat;
  content: '';
  width: 20px;
  height: 20px;
  margin-top: 10px;
}
.link {
  width: 210px;
}
.list-item:nth-child(1) {
  margin-top: 55px;
}
.list-item:nth-child(1)::before {
  background-image: url('/src/assets/images/icons/Logo-0.svg');
}
.list-item:nth-child(2)::before {
  background-image: url('/src/assets/images/icons/Logo-1.svg');
}
.list-item:nth-child(3)::before {
  background-image: url('/src/assets/images/icons/Logo-2.svg');
}
.list-item:nth-child(4)::before {
  background-image: url('/src/assets/images/icons/Logo-3.svg');
}
.list-item:nth-child(5)::before {
  background-image: url('/src/assets/images/icons/Logo-4.svg');
}
.list-item:nth-child(6)::before {
  background-image: url('/src/assets/images/icons/Logo-5.svg');
}
.list-item:nth-child(7)::before {
  background-image: url('/src/assets/images/icons/Logo-6.svg');
}
.list-item:nth-child(8)::before {
  background-image: url('/src/assets/images/icons/Logo-7.svg');
}

.burger-icon {
  cursor: pointer;
}
</style>
