<template>
  <div
    v-if="!success"
    class="bg-white md:w-fit md:rounded-3xl flex items-center"
  >
    <div class="md:p-10">
      <div class="px-6 py-6 md:p-0">
        <span
          class="text-[#ff693b] text-[40px] font-semibold md:font-bold md:text-[45px]"
        >
          Fique por dentro!
        </span>
      </div>
      <Check />
      <Email @submit="submitForm" />
    </div>
<div :class="animate" class="w-[400px] flex justify-center flex-shrink-0 h-[593px] bg-gradient-to-r from-pink-500 to-[#ff4a3d]   rounded-2xl">
  <img class="md:flex hidden" src="../assets/email-campaign-bro.svg" alt="" @load="animate=''"  loading="lazy"/>

</div>    <div class="flex items-center w-full">
      <img class="md:hidden w-full flex" src="../assets/mobil.svg" alt="" loading="lazy" />
    </div>
  </div>
  <div v-else>
    <Success v-bind:email="email"/>
  </div>
</template>

<script setup>
import Success from "../pages/succesPage.vue";
import Check from "../components/checkPart.vue";
import Email from "../components/emailPart.vue";
import { ref } from "vue";

const success = ref(false);
const animate = ref('animate-pulse')
const email = ref("");

function submitForm() {
  console.log("form submitted");
  success.value = true;
}

function handleEmailSubmission(submittedEmail) {
  email.value = submittedEmail;
  success.value = true;
}
</script>

<style></style>
