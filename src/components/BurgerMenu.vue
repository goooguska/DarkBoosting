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
        <li class="list-item" v-for="(item, i) of items" :key="i">
          <RouterLink class="link" :to="item.url">{{ item.name }} </RouterLink>
        </li>
      </ul>
    </transition>
  </div>
</template>

<script setup>
import { defineProps, ref } from 'vue'
let show = ref(false)

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
</script>

<style scoped>
ul {
  list-style: none;
}
a {
  text-decoration: none;
}
.list-enter-active,
.list-leave-active {
  transition: opacity 0.5s ease;
}

.list-enter-from,
.list-leave-to {
  opacity: 0;
}
.burger-list {
}
.list-item {
  display: flex;
  align-items: center;
}
.list-item::before {
  content: '';
  display: inline-block;

  margin-right: 10px;
}
.list-item:nth-child(1)::before {
  background-image: url('/src/assets/images/icons/lol.svg');
}
.list-item:nth-child(2)::before {
  background-image: url('/src/assets/images/icons/wowClassic.svg');
}
.list-item:nth-child(3)::before {
  background-image: url('/src/assets/images/icons/hearthstone.svg');
}
.list-item:nth-child(4)::before {
  background-image: url('/src/assets/images/icons/valorant.svg');
}
.list-item:nth-child(5)::before {
  background-image: url('/src/assets/images/icons/dota.svg');
}
.list-item:nth-child(6)::before {
  background-image: url('/src/assets/images/icons/overwatch.svg');
}
.list-item:nth-child(7)::before {
  background-image: url('/src/assets/images/icons/csgo.svg');
}
.list-item:nth-child(8)::before {
  background-image: url('/src/assets/images/icons/wowBfa.svg');
}

.burger-icon {
  cursor: pointer;
}
</style>
