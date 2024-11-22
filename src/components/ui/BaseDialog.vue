<template>
  <section
    class="flex flex-col justify-start items-start p-14 max-w-[28rem] space-y-5 text-[#222742]"
  >
    <img src="../../assets/images/icon-success.svg" alt="" class="h-16" />
    <h2 class="roboto-bold text-[3rem] leading-none">
      Thanks for subscribing!
    </h2>
    <p class="text-[0.9rem] pb-4">
      A confirmation email has been sent to ash@loremcompany.com. Please open it
      and click the button inside to confirm your subscription.
    </p>
    <base-button @click="dismissDialog">Dismiss message</base-button>
  </section>
</template>

<script setup>
import { inject } from "vue";
import BaseButton from "./BaseButton.vue";

const emit = defineEmits(["dismiss"]);

function dismissDialog() {
  emit("dismiss");
}
</script>
