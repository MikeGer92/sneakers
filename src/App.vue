<script setup>
import Header from './components/icons/Header.vue'
import CardsList from './components/CardsList.vue'
import Drawer from './components/Drawer.vue'
</script>

<template>
  <Drawer />
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
    <Header></Header>

    <div class="p-10">
      <h2 class="text-3xl font-bold mb-5">Все кроссовки</h2>
      <CardsList />
    </div>
  </div>
</template>

<style scoped></style>
