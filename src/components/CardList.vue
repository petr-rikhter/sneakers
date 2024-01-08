<script setup>
import { ref } from 'vue'
import CardItem from './CardItem.vue'
import CartItem from './CartItem.vue'

defineProps({
  title: String,
  typeOfComponent: String
})

let isAdded = ref(false)
let isFavorite = ref(false)
let isDeleted = ref(false)

const onClickAdded = () => (isAdded.value = !isAdded.value)
const onClickFavorite = () => (isFavorite.value = !isFavorite.value)
const onClickDeleted = () => (isDeleted.value = !isDeleted.value)
</script>

<template>
  <div class="p-1">
    <h2 v-if="title" class="text-3xl font-bold">{{ title }}</h2>
    <div class="flex flex-wrap gap-3 mt-5">
      <component
        :is="typeOfComponent === 'CardItem' ? CardItem : CartItem"
        imageUrl="/sneakers/sneakers-1.jpg"
        title="Мужские кроссовки"
        model="Nike Blazer Mid Suede"
        :price="12990"
        :onClickAdded="onClickAdded"
        :onClickFavorite="onClickFavorite"
        :onClickDeleted="onClickDeleted"
      ></component>
    </div>
  </div>
</template>
