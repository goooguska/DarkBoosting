<script setup>
import { defineProps, ref } from 'vue'
const show = ref(false)
defineProps({
  items: {
    type: Array,
    required: true
  },
  type: {
    type: String,
    required: true,
    default: 'lang'
  }
})
</script>
<template>
  <div class="dropdown">
    <div class="dropdown-content" @mouseenter="show = true" @mouseleave="show = false">
      <div class="icons">
        <slot />
        <svg
          width="10"
          height="10"
          viewBox="0 0 10 10"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M0.833984 3.3335L5.00065 7.50016L9.16732 3.3335H0.833984Z" fill="#171026" />
        </svg>
      </div>

      <ul class="list" v-show="show">
        <li class="list-item" v-for="(item, i) of items" :key="i">
          <span v-if="type === 'lang'" to="">{{ item }}</span>

          <RouterLink v-if="type === 'link'" :to="item.url"> {{ item.name }} </RouterLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
a {
  text-decoration: none;
  color: var(--color-font-primary);
}
.dropdown {
  position: relative;
  display: flex;
  align-items: center;
  gap: 4px;
}
.dropdown-content {
  min-height: 50px;
  position: relative;
  display: flex;
  align-items: center;
  gap: 4px;
  z-index: 2;
}
.icons {
  display: flex;
  align-items: center;
  gap: 4px;
}
.list {
  background-image: url('/src/assets/images/backgrounds/dropdownBG.jpg');
  position: absolute;
  top: 100%;
  left: -65%;
  z-index: 3;
  list-style: none;
}
.list-item {
  cursor: pointer;
  padding: 15px 30px;
  font-size: 16px;
  font-weight: 400;
  font-family: 'Fira Sans';
}
.list-item:nth-child(1) {
  padding-top: 20px;
}
.list-item:nth-child(5) {
  font-weight: 500;
}
.list-item:hover {
  opacity: 0.4;
  background: radial-gradient(50% 50% at 50% 50%, rgba(255, 255, 255, 0) 0%, #a1a1a1 100%), #e6e6e6;
}
</style>
