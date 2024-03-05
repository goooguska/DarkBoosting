<script setup>
import ClientsReviewSidebar from "./ClientsReviewSidebar.vue";
import ClientsReviewCards from "./ClientsReviewCards.vue";
</script>

<template>
    <div class="content">
        <div class="container">
        <ClientsReviewSidebar/>
        <ClientsReviewCards/>
        </div>
    </div>
    
</template>

<style scoped>
.content{
    margin-top: 100px;
    background-image: url('/src/assets/images/backgrounds/clientsReviewBG.png');
    background-repeat: no-repeat;
}
.container{
    
    display: flex;
    justify-content: space-between;

}

</style>