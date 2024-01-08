<script setup>
import Header from './components/Header.vue'
import CardList from './components/CardList.vue'
import Drawer from './components/Drawer.vue'
</script>

<template>
  <Drawer />
  <div class="bg-white w-4/5 m-auto mt-14 rounded-xl shadow-xl">
    <Header />
    2,47,56

    <CardList title="Все кроссовки" type-of-component="CardItem" />
  </div>
</template>

<style scoped></style>
