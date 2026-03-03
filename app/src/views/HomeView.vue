<template> 
<h1> bread shop </h1>
<div class="container">

        <BreadCard v-for= "bread in breads" 
        :key="bread.name" 
        :bread="bread"/>
       <button @click="addToCart(bread)">Add to Cart</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import BreadCard from '@/components/BreadCard.vue';

function addToCart(bread) {
  console.log(bread)
}

const breads = ref([
{ name: 'strawberry jam', img:"/strberryjam.png", price:'3 coins'},
{ name: 'fresh strawberries', img:"/strberry.png", price: '2 coins' },
{ name: 'egg', price: '4 coins' },
{ name: 'banana peanut butter', price: '3 coins' },
{ name: 'blueberry jam', price: '3 coins' },
{ name: 'fresh kiwi', price:'2 coins' },
{ name: 'orange jam', price: '3 coins' },
{ name: 'raspberry jam', price: '3 coins' },
{ name: 'cherry jam', price: '3 coins' },
{ name: 'blackberry jam', price: '3 coins' },
{ name: 'peach jam', price: '3 coins' },
{ name: 'avocado', price: '4 coins' },
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
</style>