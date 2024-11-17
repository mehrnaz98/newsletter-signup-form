<template>
  <main
    class="flex min-h-screen justify-center items-center bg-[#36384D] roboto-regular"
  >
    <div class="container bg-white rounded-3xl w-auto sm:max-w-[50rem] m-5">
      <picture class="responsive-image">
        <source
          media="(min-width: 768px)"
          srcset="./assets/images/illustration-sign-up-desktop.svg"
        />
        <img src="./assets/images/illustration-sign-up-mobile.svg" alt="" />
      </picture>
      <FormSection />
    </div>
  </main>
</template>

<script setup>
import FormSection from "./components/FormSection.vue";
</script>
