<script setup>
import CardList from './CardList.vue'
</script>

<template>
  <div class="fixed top-0 left-0 w-full h-full bg-black z-10 opacity-70"></div>
  <div class="flex flex-col bg-white w-96 h-full fixed right-0 top-0 z-20 p-8">
    <div class="flex gap-3">
      <img
        src="/arrow-left.svg"
        class="w-6 opacity-30 cursor-pointer hover:opacity-100 hover:-translate-x-1"
      />
      <h2 class="text-3xl font-bold">Корзина</h2>
    </div>

    <CardList class="flex-1" type-of-component="CartItem" />

    <div class="flex flex-col gap-2 justify-between">
      <div class="flex justify-between">
        <span>Итого:</span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>21498 руб.</b>
      </div>
      <div class="flex justify-between">
        <span>Налог 5%:</span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>1074 руб.</b>
      </div>
      <button
        class="transition bg-lime-500 w-full rounded-lg py-2 text-white hover:bg-lime-600 active:bg-lime-700 disabled:bg-slate-300"
      >
        Оформить заказ
      </button>
    </div>
  </div>
</template>
