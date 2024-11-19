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
    <button
      type="submit"
      class="bg-[#232742] text-white mt-4 text-[0.8rem] p-3 rounded-md"
    >
      Subscribe to monthly newsletter
    </button>
  </form>
</template>

<script setup>
import BaseButton from "./ui/BaseButton.vue";
const emit = defineEmits(["form-submitted"]);

function submitForm() {
  emit("form-submitted");
}
</script>
