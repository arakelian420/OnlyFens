<script setup>
import Header from './components/Header.vue'
import CardList from './components/CardList.vue'
import Drawer from './components/Drawer.vue'
</script>

<template>
  <div>
    <Drawer />
    <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-20 mb-20">
      <Header />

      <div class="p-10">
        <h2 class="text-3xl font-bold mb-5">All sweets</h2>

        <CardList />
      </div>
    </div>
  </div>
</template>
