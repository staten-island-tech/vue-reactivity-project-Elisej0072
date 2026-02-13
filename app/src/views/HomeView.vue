<template>
       <h1>ksdgjasgjh</h1>
    <div class="container">
        <ToppingCard v-for="topping in toppings" :key="topping.name" :topping="topping">{{ topping.name }}</ToppingCard> 
    </div>
    
</template>

<script>
import { ref } from 'vue'

const toppings =ref([
{ name: 'sliced beef', price: ''},
{ name: 'chicken', price: ''},
{ name: 'beef balls', price: ''},
{ name: 'tripe', price: ''},
{ name: 'beansprouts', price: ''},
{ name: 'basil', price: ''},
{ name: 'mint', price: ''},
{ name: 'onions', price: ''},
{ name: 'lime', price: ''},
{ name: 'cilantro', price: ''},
{ name: 'jalapenos', price: ''},
])

</script>

<style scoped>

</style>