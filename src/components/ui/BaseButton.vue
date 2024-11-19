<template>
  <button
    :type="type"
    class="bg-[#232742] text-white mt-4 text-[0.8rem] p-3 rounded-md"
  >
    <slot />
  </button>
</template>

<script setup>
import { defineProps } from "vue";
</script>
