<script setup>
import Order from "../components/Order.vue";

//把下單後的訂單資料顯示在網頁上 並可以做刪除訂單的動作
const Orders = [
  { num: "12345678", name: "812020", number: "83233" },
  { num: "9210290", name: "829393", number: "83201" },
];
</script>

<template>
  <div>
    <div
      class="w-screen h-[40px] bg-[#D9D9D9] font-thin text-[20px] flex justify-center items-center"
    >
      商品預約情況
    </div>
    <div class="mt-[20px]">
      <Order
        v-for="Order in Orders"
        :key="Order.num"
        :num="Order.num"
        :name="Order.name"
        :number="Order.number"
      />
    </div>
  </div>
</template>
