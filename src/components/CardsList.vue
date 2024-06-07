<script setup>
import Card from './Card.vue'
const onClickAdded = () => {
  alert('Добавить')
}
</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <Card :isFavorite="false" @click="onClickAdded" />
    <Card />
    <Card />

  </div>
</template>
