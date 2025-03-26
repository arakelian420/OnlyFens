<script setup>
import DrawerHead from "./DrawerHead.vue";
import BracketItemList from "./BracketItemList.vue";

const onClickDelete = () => {
  alert("Deleted from cart");
};
</script>

<template>
  <div>
    <div
      class="bg-black z-10 fixed top-0 left-0 h-full w-full opacity-75"
    ></div>
    <div class="bg-white w-128 h-full fixed right-0 top-0 z-20 p-8">
      <DrawerHead />
      <BracketItemList />

      <div class="flex flex-col gap-4 mt-7">
        <div class="flex gap-2">
          <span>Total:</span>
          <div class="flex-1 border-b border-dashed opacity-30"></div>
          <b>299 USD</b>
        </div>

        <div class="flex gap-2">
          <span>VAT 5%:</span>
          <div class="flex-1 border-b border-dashed opacity-30"></div>
          <b>23 USD</b>
        </div>

        <button
          class="transition bg-lime-500 w-full rounded-xl py-3 text-white hover:bg-lime-600 disabled:bg-slate-300 active:bg-lime-400 cursor-pointer"
        >
          Order
        </button>
      </div>
    </div>
  </div>
</template>
