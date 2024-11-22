<template>
  <form @submit.prevent="submitForm" class="flex flex-col">
    <label for="email" class="roboto-bold text-[0.7rem] mt-7"
      >Email address</label
    >
    <input
      type="email"
      id="email"
      class="mt-2 border border-[#B3B2B7] text-[0.8rem] p-3 rounded-md"
      placeholder="email@company.com"
    />
    <base-button type="submit"> Subscribe to monthly newsletter </base-button>
  </form>
</template>

<script setup>
import { reactive } from "vue";
import BaseButton from "./ui/BaseButton.vue";
const emit = defineEmits(["form-submitted"]);

function submitForm() {
  emit("form-submitted");
}
</script>
