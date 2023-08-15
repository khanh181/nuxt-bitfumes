<template>
  <div>
    <NuxtPage />
    <a href="#" @click="view('home')">Home</a>
    <a href="#" @click="view('counter')">Counter</a>
    <!-- <HelloWellcome /> -->
    <button @click="toggle">toggle</button>
    <!-- <component :is="current" /> -->

    <LazyHelloWellcome v-if="page === 'home'" />
    <LazyCounter v-if="page === 'counter'" />
  </div>
</template>

<script setup>
const page = ref("home");
const current = shallowRef(resolveComponent("Counter"));

function view(name) {
  page.value = name;
}
const toggle = () => {
  current.value = resolveComponent("HelloWellcome");
};
</script>
