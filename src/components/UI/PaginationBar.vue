

<script setup>

</script>

<template>
   <div class="pagination">
            <img class="pagination-bar" src="/src/assets/images/img/pagination-panel.png" alt="#">
            <p class="pagination-text"> <span class="pagination-current">4 </span>/ 16 </p>
        </div>
</template>

<style scoped>
.pagination-text{
    font-family: "Fira Sans";
    font-size: 16px;
    font-weight:400;
    color: var(---color-font-more);
}
.pagination-current{
    margin-left: 22px;
    font-family: "Fira Sans";
    font-size: 30px;
    font-weight:500;
    color: var(--color-font-numbers);
}
.pagination{
    align-items: center;
    display: flex;
}
.pagination-bar{
    height: 5px;
}
</style>