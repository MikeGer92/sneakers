<script setup>
defineProps({
  imageUrl: String,
  title: String,
  price: Number,
  isFavorite: Boolean,
  isAdded: Boolean,
  onClickAdd: Function,
  onClickFavorite: Function
})
</script>

<template>
  <div>
    <div
      class="relative border border-slate-200 rounded-3xl p-8 cursor-pointer hover:-translate-y-2 hover:shadow-xl transition"
    >
      <img
        :src="isFavorite ? '/like_2.svg' : '/like_1.svg'"
        alt="Like-2"
        class="absolute top-8 left-8"
        @click="onClickFavorite"
      />
      <img src="/sneakers/sneakers-1.jpg" alt="Sneaker" />
      <p class="mt-2">{{ title }}</p>

      <div class="flex justify-between">
        <div class="flex flex-col mt-5">
          <span class="text-slate-400">Цена:</span>
          <b>{{ price }} руб.</b>
        </div>
        <img :src="!isAdded ? '/plus.svg' : '/checked.svg'" alt="Plus" @click="onClickAdd" />
      </div>
    </div>
  </div>
</template>
