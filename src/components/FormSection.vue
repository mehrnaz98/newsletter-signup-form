<template>
  <div class="bg-white rounded-3xl w-auto sm:max-w-[50rem] m-5">
    <div class="container" v-if="!isDialogVisible">
      <picture class="responsive-image">
        <source
          media="(min-width: 768px)"
          srcset="../assets/images/illustration-sign-up-desktop.svg"
        />
        <img src="../assets/images/illustration-sign-up-mobile.svg" alt="" />
      </picture>
      <div class="form-section space-y-3">
        <h1 class="text-[2.8rem] roboto-bold">Stay updated!</h1>
        <p class="text-[0.9rem]">
          Join 60,000+ product managers receiving monthly updates on:
        </p>
        <ul class="custom-list text-[0.9rem]">
          <li>Product discovery and building what matters</li>
          <li>Measuring to ensure updates are a success</li>
          <li>And much more!</li>
        </ul>
        <TheForm @form-submitted="showDialog" />
      </div>
    </div>
    <BaseDialog v-if="isDialogVisible" @dismiss="hideDialog" />
  </div>
</template>

<script setup>
import { provide, ref } from "vue";
import TheForm from "./TheForm.vue";
import BaseDialog from "./ui/BaseDialog.vue";

const email = ref("");
const isDialogVisible = ref(false);

function showDialog() {
  isDialogVisible.value = true;
}

function hideDialog() {
  isDialogVisible.value = false;
}
</script>
