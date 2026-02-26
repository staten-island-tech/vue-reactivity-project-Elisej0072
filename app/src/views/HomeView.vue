<template>
       <h1>ksdgjfjfhfh</h1>
    <div class="container">
        <ToppingCard v-for="topping in toppings" 
        :key="topping.name" 
        :topping="topping">{{ topping.name }}</ToppingCard>
         
    </div>
    
</template>

<script>
import { ref } from 'vue'
import ToppingCard from '@/components/ToppingCard.vue';

const toppings = ref([
{ name: 'sliced beef', price: ''},
{ name: 'chicken', price: ''},
{ name: 'ribeye', price: ''},
{ name: 'oxtail', price: ''},
{ name: 'shrimp', price: ''},
{ name: 'seafood', price: ''},
{ name: 'beef balls', price: ''},
{ name: 'fish balls', price: ''},
{ name: 'beef tendon', price: ''},
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
div {
  padding: 16px;
}

h1 {
  text-align: center;
  margin-bottom: 20px;
}
.container {
  display: flex;
  width: 80vw;
  margin: 20px auto;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
}
.card {
  border: 1px solid #ccc;
  padding: 12px;
  margin-bottom: 12px;
  border-radius: 6px;
  width: 300px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
</style>