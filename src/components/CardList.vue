<script setup>
import Card from './Card.vue'

const onClickAdd = () => {
  alert('Add to cart')
}

const onClickFavourite = () => {
  alert('Add to favourite')
}
</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
      title="Hot Chili Sausages"
      :price="29"
      imageUrl="/sneakers/sneakers-1.jpg"
      :onClickAdd="onClickAdd"
      :onClickFavourite="onClickFavourite"
    />
  </div>
</template>
