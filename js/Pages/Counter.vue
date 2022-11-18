<script setup>
import { ref } from "vue";

const count = ref(0);

const addCount = () => {
    count.value = count.value + 1;
};
</script>

<template>
    <h2>Counter</h2>
    <p>Count:{{ count }}</p>
    <button class="count" @click="addCount">Add</button>
</template>

<style scoped>
h2 {
  color: rgba(91, 139, 183, 0.7);
}
.count {
  margin: 0 auto;
  padding: 5px;
  width: 60px;
  color: white;
  background-color: rgba(36, 139, 105, 0.6);
  border-radius: 6px;
  border-style: none;
  cursor: pointer;
}
</style>