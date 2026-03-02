<template> 
<h1>ksdgjfjfhfh</h1>
<div class="container">
        <BreadCard v-for= "bread in breads" 
        :key="bread.name" 
        :breads="bread">
        <button @click="addToCart(bread)">Add to Cart</button>
      </BreadCard>
    </div>
</template>

<script>
import { ref } from 'vue'

import BreadCard from '@/components/BreadCard.vue';

function addToCart(bread) {
  console.log(bread)
}

const breads = ref([
{ name: 'bred' , price: 1 },
{ name: 'bred1', price: 1 },
{ name: 'bred2', price: 1 },
{ name: 'bred3', price: 1 },
{ name: 'bred4', price: 1 },
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