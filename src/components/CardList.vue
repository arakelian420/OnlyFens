<script setup>
import Card from "./Card.vue";

defineProps({
  items: Array,
});

const onClickAdd = () => {
  alert("Add to cart");
};

const onClickFavourite = () => {
  alert("Add to favourite");
};
</script>

<template>
  <div class="grid grid-cols-4 gap-5 mt-8">
    <Card
      v-for="item in items"
      :key="item.id"
      :title="item.title"
      :price="item.price"
      :imageUrl="item.imageUrl"
      :onClickAdd="onClickAdd"
      :onClickFavourite="onClickFavourite"
    />
  </div>
</template>
