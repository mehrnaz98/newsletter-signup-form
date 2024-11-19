<template>
  <section
    class="flex flex-col justify-start items-start p-14 max-w-[28rem] space-y-5 text-[#222742]"
  >
    <img src="../../assets/images/icon-success.svg" alt="" class="h-16" />
    <h2 class="roboto-bold text-[3rem] leading-none">
      Thanks for subscribing!
    </h2>
    <p class="text-[0.9rem]">
      A confirmation email has been sent to ash@loremcompany.com. Please open it
      and click the button inside to confirm your subscription.
    </p>
    <button @click="dismissDialog">Dismiss message</button>
  </section>
</template>

<script setup>
const emit = defineEmits(["dismiss"]);

function dismissDialog() {
  emit("dismiss");
}
</script>
