<script setup>
import Header from "./components/Header.vue";
import CardList from "./components/CardList.vue";
import Drawer from "./components/Drawer.vue";
</script>

<template>
  <div>
    <!-- <!Drawer /> -->
    <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-20 mb-20">
      <Header />

      <div class="p-10">
        <div class="flex justify-between items-center">
          <h2 class="text-3xl font-bold mb-5">All sweets</h2>

          <div class="flex gap-4">
            <select
              class="py-2 px-3 border rounded-xl border-gray-300 text-gray-500"
            >
              <option>By name</option>
              <option>By price (low to high)</option>
              <option>By price (high to low)</option>
            </select>

            <div class="relative">
              <img class="absolute left-4 top-3" src="/search.svg" alt="" />
              <input
                class="border rounded-xl py-2 pl-10 pr-4 outline-none focus:border-gray-400 border-gray-300"
                placeholder="Search..."
              />
            </div>
          </div>
        </div>
        <CardList />
      </div>
    </div>
  </div>
</template>
