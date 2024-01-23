<template>
  <div class="dropdown" @mouseenter="show = true" @mouseleave="show = false">
    <slot />
    <img src="@/assets/images/icons/arrow-down.svg" alt="#" />

    <ul class="list" v-if="show">
      <li class="list-item" v-for="(item, i) of items" :key="i">
        <span v-if="type === 'lang'" to="">{{ item }}</span>

        <RouterLink v-if="type === 'link'" :to="item.url"> {{ item.name }} </RouterLink>
      </li>
    </ul>
  </div>
</template>

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
.list {
  text-align: center;
  position: absolute;

  top: 100%;

  list-style: none;
}
.list-item {
  font-size: 16px;
  font-weight: 500;
  font-family: 'Fira Sans';
}
</style>
