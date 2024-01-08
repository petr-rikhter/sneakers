<script setup></script>

<template>
  <header class="flex justify-between border-b border-slate-300 px-8">
    <div class="left flex items-center gap-4">
      <img src="/logo.png" alt="Logo" class="w-10" />
      <div>
        <h1 class="text-xl font-bold uppercase">VUE SNEAKERS</h1>
        <p class="text-slate-500">Магазин лучших кроссовок</p>
      </div>
    </div>

    <ul class="right flex gap-4">
      <li
        @click="onCartClickHandler"
        class="flex items-center gap-3 cursor-pointer text-gray-500 hover:text-black"
      >
        <img src="/cart.svg" alt="cart" />
        <b>1205 руб.</b>
      </li>
      <li class="flex items-center gap-3 cursor-pointer hover:text-black">
        <img src="/heart.svg" alt="bookmarks" />
        <span class="text-gray-500 hover:text-black">Закладки</span>
      </li>
      <li class="flex items-center gap-3 cursor-pointer hover:text-black">
        <img src="/profile.svg" alt="profile" />
        <span class="text-gray-500 hover:text-black">Профиль</span>
      </li>
    </ul>
  </header>
</template>
