<template>
  <button
    :type="type"
    class="bg-[#232742] w-[100%] text-white mt-4 text-[0.8rem] p-3 rounded-md hover:bg-[#FF6740] transition-colors ease-in-out duration-300"
  >
    <slot />
  </button>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  type: {
    type: String,
    default: "button",
  },
});
</script>
