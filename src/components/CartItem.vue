<script setup>
defineProps({
  imageUrl: String,
  title: String,
  model: String,
  price: Number,
  onClickDeleted: Function
})
</script>

<template>
  <div class="border rounded-cart border-slate-100 p-4 hover:shadow-xl transition">
    <div class="flex items-end gap-2">
      <img :src="imageUrl" alt="Sneaker" class="w-20" />
      <div class="flex flex-col">
        <p>{{ title }}</p>
        <p>{{ model }}</p>
        <b>{{ price }} руб.</b>
      </div>

      <div class="flex justify-between mt-5">
        <img
          @click="onClickDeleted"
          class="opacity-70 hover:opacity-100 cursor-pointer"
          src="/close.svg"
          alt="Remove"
        />
      </div>
    </div>
  </div>
</template>
