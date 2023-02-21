<template>
  <div class="about">
    <h1>About</h1>
    <button class="counter-btn" @click="storeCount.increaseCount ">
      {{ storeCount.count }}
    </button>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter';

const storeCount = useCounterStore()

</script>

<style>
.counter-btn{
  font-size: 50px;
}
</style>