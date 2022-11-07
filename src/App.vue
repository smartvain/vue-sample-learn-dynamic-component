<script setup lang="ts">
import { ref } from 'vue';
import ComponentA from './components/ComponentA.vue'
import ComponentB from './components/ComponentB.vue'

const comp = ref(ComponentA)
</script>

<template>
  <button @click="comp = ComponentA">ComponentA</button>
  <button @click="comp = ComponentB">ComponentB</button>
  <keep-alive>
    <component :is="comp" />
  </keep-alive>
</template>

<style scoped>
</style>
