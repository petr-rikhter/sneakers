<script setup>
import { ref } from 'vue'

defineProps({
  imageUrl: String,
  title: String,
  model: String,
  price: Number,
  onClickAdded: Function,
  onClickFavorite: Function
})

let isFavorite = ref(false)
let isAdded = ref(false)
</script>

<template>
  <div
    class="relative border rounded-card border-slate-100 p-10 cursor-pointer hover:shadow-xl hover:-translate-y-2 transition"
  >
    <img
      @click="onClickFavorite"
      class="absolute"
      :src="isFavorite ? '/like-2.svg' : '/like-1.svg'"
      alt="Like"
    />
    <img :src="imageUrl" alt="Sneaker-1" class="w-full" />
    <p>{{ title }}</p>
    <p>{{ model }}</p>
    <div class="flex justify-between mt-5">
      <div>
        <p class="text-gray-500">Цена:</p>
        <b>{{ price }} руб.</b>
      </div>
      <img @click="onClickAdded" :src="isAdded ? '/checked.svg' : '/plus.svg'" alt="Plus" />
    </div>
  </div>
</template>
