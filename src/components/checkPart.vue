<template>
  <div class="w-[400px] px-6 md:p-0">
    <span class="text-center text-base"
      >Junte-se a  mais de 60,000 Product Managers recebendo updetes mensais em:</span
    >
    <div class="py-4">
      <div
        class="check flex py-2 space-x-4"
        v-for="(item, index) in dataTable"
        :key="index"
      >
        <img src="../assets/check.svg" alt="" />
        <span>
          {{ item.title }}
        </span>
      </div>
    </div>
  </div>
</template>

<script setup>
const dataTable = [
  {
    title: "Descoberta de produtos e construção do que realmente importa",
  },
  {
    title: "Medindo para garantir que as atualizações sejam bem-sucedidas",
  },
  {
    title: "E muito mais!",
  }
];
</script>

<style></style>
