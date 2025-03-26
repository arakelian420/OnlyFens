<script setup>
import DrawerHead from './DrawerHead.vue'
import BracketItem from './BracketItem.vue'

const onClickDelete = () => {
  alert('Deleted from cart')
}
</script>

<template>
  <div>
    <div class="bg-black z-10 fixed top-0 left-0 h-full w-full opacity-75"></div>
    <div class="bg-white w-128 h-full fixed right-0 top-0 z-20 p-8">
      <DrawerHead />
      <BracketItem
        title="Hot Chili Sausages"
        :price="29"
        imageUrl="/sneakers/sneakers-1.jpg"
        :onClickDelete="onClickDelete"
      />
      <BracketItem
        title="Hot Chili Sausages"
        :price="29"
        imageUrl="/sneakers/sneakers-1.jpg"
        :onClickDelete="onClickDelete"
      />
    </div>
  </div>
</template>
