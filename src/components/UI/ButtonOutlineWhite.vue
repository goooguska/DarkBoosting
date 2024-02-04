<template>
  <div class="button" >
    <slot  />
  </div>
</template>

<script setup></script>

<style scoped>

.button{
  cursor: pointer;
  display: inline-block;
  border-radius: 0px 30px;
  padding: 25px 30px;
  border: 2px solid var(--color-font-secondary);
  font-size: 18px;
  font-weight:700;
  color: var(--color-font-secondary);
}
.button:hover{
  color:var(  --color-font-primary) ;
  background-image: url('/src/assets/images/backgrounds/transparent-white-smoke-2.png');

}
</style>
