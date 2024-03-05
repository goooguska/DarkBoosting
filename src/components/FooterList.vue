<script setup>
defineProps({
    items:{
        type:Array,
        required:true
    },
    icons:{
        type:Array,
        required:true
    },
  

})
</script>

<template>
    <ul class="list"  v-for="(item,i) of items" :key="i" >
        <li class="title">{{ item.title }} </li> 
        <li class="points" v-for="(point,i) of item.points" :key="i">{{point}} </li> 
    </ul>
   <ul class="list-icons"  v-for="(icon,i) of icons" :key="i">
        <li class="title"> {{icon.title  }}</li>
        <li class=" icons">
            <img v-for="(point,i) of icon.iconsMedia" :key="i" :src="point"/> 
        </li>
   </ul>

  


</template>


<style scoped>
ul{
    list-style: none;
}
.title{
    font-family: "Fira Sans";
    font-weight: 700;
    font-size: 20px;
    text-transform: uppercase;
    color: var(--color-font-secondary);


}
.icons:nth-child(2),
.points:nth-child(2){
    padding-top: 20px;
}
.points{
    font-family: "Fira Sans";
    font-weight: 400;
    font-size: 16px;
    color: var(--color-font-secondary);
    padding-bottom: 20px;
    opacity: 0.6;
}
.icons{
    display: flex;
    gap: 20px;
}

</style>