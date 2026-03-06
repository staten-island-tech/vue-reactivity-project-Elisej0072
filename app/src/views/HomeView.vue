<template> 
<h1> bread shop :3 </h1>
<div class="container">
        <BreadCard v-for= "bread in breads" 
        :key="bread.name" 
        :bread="bread"/>  
    </div>

</template>

<script setup>

import { ref } from 'vue'
import BreadCard from '@/components/BreadCard.vue';
import ItemCart from '@/components/ItemCart.vue';

const breads = ref([
{ name: 'strawberry jam', img:"/strberryjam.png", price:'3 coins'},
{ name: 'fresh strawberries', img:"/strberry.png", price: '2 coins' },
{ name: 'egg', img:"/egg.png", price: '4 coins' },
{ name: 'banana', img:"/banana.png", price: '3 coins' },
{ name: 'blueberry jam', img:"/blberry.png", price: '3 coins' },
{ name: 'fresh kiwi', img:"/kiwi.png", price:'2 coins' },
{ name: 'orange jam', img:"/orange.png", price: '3 coins' },
{ name: 'raspberry jam', img:"/raberry.png", price: '3 coins' },
{ name: 'cherry jam', img:"/cherry.png", price: '3 coins' },
{ name: 'blackberry jam', img:"/bkberry.png", price: '3 coins' },
{ name: 'peach jam', img:"/peach.png", price: '3 coins' },
{ name: 'avocado', img:"/avocado.png", price: '4 coins' },
])

const cart = ref([])
function addToCart(bread) {
cart.value.push(bread);
console.log("bread.name", "bread.price");
}

</script>


<style scoped>
div {
  padding: 17px;
}

h1 {
  text-align: center;
  margin-bottom: 2px;
}
.container {
  display: flex;
  width: 80vw;
  margin: 2px auto;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  
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
.button{
  justify-content: space-around;
  align-items: center;
}
</style>