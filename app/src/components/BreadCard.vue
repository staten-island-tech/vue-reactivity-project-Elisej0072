<template>
    <div>
<h2> {{ bread.name }}</h2>
<h3>{{ bread.price }}</h3>
<img :src="bread.img" alt= "" />
    </div>
</template>

<script setup>
   defineProps({
            bread:{
            type: Object,
            required: true
        },
    })
</script>

<style scoped>
div{
    display:flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    height: 300px;
    width: 200px;
    border: 6px solid rgba(155, 109, 79, 0.418);
    margin-top: 15px ;
}
</style>