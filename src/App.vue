<script setup>
import Header from "./components/Header.vue";
import CardList from "./components/CardList.vue";
import Drawer from "./components/Drawer.vue";
import { onMounted, ref, watch } from "vue";
import axios from "axios";

const items = ref([]);

const sortBy = ref("");
const searchQuery = ref("");

const onChangeSelect = (event) => {
  sortBy.value = event.target.value;
};

onMounted(async () => {
  try {
    const { data } = await axios.get(
      "https://604781a0efa572c1.mokky.dev/items"
    );
    items.value = data;
  } catch (error) {
    console.error(error);
  }
});

watch(sortBy, async () => {
  try {
    const { data } = await axios.get(
      `https://604781a0efa572c1.mokky.dev/items?sortBy=${sortBy.value}`
    );
    items.value = data;
  } catch (error) {
    console.error(error);
  }
});
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
              @change="onChangeSelect"
              class="py-2 px-3 border rounded-xl border-gray-300 text-gray-500"
            >
              <option value="name">By name</option>
              <option value="price">By price (low to high)</option>
              <option value="-price">By price (high to low)</option>
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

        <CardList :items="items" />
      </div>
    </div>
  </div>
</template>
