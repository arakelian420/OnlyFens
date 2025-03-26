<script setup>
defineProps({
  imageUrl: String,
  title: String,
  price: Number,
  isFavourite: Boolean,
  isAdded: Boolean,
  onClickDelete: Function,
});
</script>

<template>
  <div
    class="grid items-center grid-flow-col grid-rows-2 grid-cols-8 gap-4 m-3 bg-white relative h-35 border border-slate-200 rounded-3xl p-8 pb-14 cursor-pointer transition hover:-translate-y-2 hover:shadow-xl"
  >
    <div class="row-span-2 col-span-3 ...">
      <img :src="imageUrl" alt="Meal" />
    </div>
    <p class="col-span-5 mt-7">{{ title }}</p>
    <b class="row-span-1 col-span-3 mt-14">{{ price }} USD</b>

    <button
      @click="onClickDelete"
      alt="Delete"
      class="bg-red-50 h-10 w-12 row-span-1 col-span-2 ... mt-15 ml-10 rounded-xl hover:shadow-xl hover:bg-red-400 transition"
    >
      X
    </button>
  </div>
</template>
