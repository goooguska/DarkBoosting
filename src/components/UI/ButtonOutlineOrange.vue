<template>
    <div class="button" >
      <slot/>
    </div>
  </template>
  
  <script setup></script>
  
  <style scoped>
  
  .button{
    cursor: pointer;
    display: flex;
    align-items: center;
    border-radius: 0px 30px;
    padding: 25px 30px;
    border: 2px solid var(--color-font-third);
    font-size: 18px;
    font-weight:700;
    color: var(--color-font-third);
  }

.button::before{
    margin-right: 10px;
    content: '';
    display: block;
    width: 21px;
    height: 24px;
    background-image: url('/src/assets/images/icons/play.svg');
  }
  </style>
  