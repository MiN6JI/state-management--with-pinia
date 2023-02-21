<template>
  <div class="home">
    <div class="btn">
      <Counter />
      <button @click="storeCount.increaseCount">+</button>
      <button @click="storeCount.decreaseCount">-</button>
    </div>
    <hr>
    <div style="margin: 50px;">
      This counter is: {{ storeCount.oddOrEven }}
    </div>
    <hr>
    <div>
      <h3>Edit Counter: </h3>
      <input type="number" v-model="storeCount.count"> 
    </div>
  </div>
</template>

<script setup>
import Counter from '@/components/Counter.vue'
import {useCounterStore} from '@/stores/counter'


const storeCount = useCounterStore() 
</script>

<style>
.count{
  font-size: 60px;
  margin: 20px;
}
.btn button{
  width: 50px;
  font-size: 40px;
  margin: 10px;
}
</style>