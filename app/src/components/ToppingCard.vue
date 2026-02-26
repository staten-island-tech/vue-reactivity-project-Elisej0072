<template>
    <div>
<h2> {{ topping.name }}</h2>
<h3>{{ topping.price }}</h3>
<img: scr="topping.img"></img:>
    </div>
</template>

<script>
   defineProps({
        topping:{
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
    border: 3px solid black
}
</style>