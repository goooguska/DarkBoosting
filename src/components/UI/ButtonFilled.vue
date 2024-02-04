<template>
    <div class="button" >
      <slot/>
    </div>
  </template>
  
  <script setup></script>
  
  <style scoped>
  
  .button{
    cursor: pointer;
    display: inline-block;
    border-radius: 0px 30px;
    padding: 25px 30px;
    background-color:var(--color-font-third) ;
    font-size: 18px;
    font-weight:700;
    color: var(--color-font-secondary);
  }
 

  </style>
  