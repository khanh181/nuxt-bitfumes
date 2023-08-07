<template>
  <div>
    <p>Count number</p>
    <button @click="increment">+</button>
    <p>{{ count }}</p>
    <button @click="decrement">-</button>
  </div>
</template>

<script setup>
const count = ref(0);

const decrement = () => {
  count.value--;
};

const increment = () => {
  count.value++;
};
</script>

<style lang="scss" scoped></style>
