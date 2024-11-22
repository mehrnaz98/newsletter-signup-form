<template>
  <form @submit.prevent="submitForm" novalidate class="flex flex-col">
    <div class="flex items-center justify-between mt-7">
      <label for="email" class="roboto-bold text-[0.7rem]">
        Email address
      </label>
      <p v-if="!email.isValid" class="text-red-600 text-[0.7rem]">
        Valid email required
      </p>
    </div>
    <input
      v-model="email.val"
      type="email"
      id="email"
      :class="[
        'mt-2 border text-[0.8rem] p-3 rounded-md',
        email.isValid
          ? 'border-[#B3B2B7] bg-white text-black'
          : 'border-red-600 bg-red-100 text-red-600',
      ]"
      placeholder="email@company.com"
      @blur="validateForm"
    />

    <base-button type="submit"> Subscribe to monthly newsletter </base-button>
  </form>
</template>

<script setup>
import { reactive, provide } from "vue";
import BaseButton from "./ui/BaseButton.vue";
const emit = defineEmits(["form-submitted"]);

const email = reactive({
  val: "",
  isValid: true,
});

const formIsValid = reactive({
  value: true,
});

function validateForm() {
  formIsValid.value = true;
  if (email.val === "" || !email.val.includes("@")) {
    email.isValid = false;
    formIsValid = false;
  } else {
    email.isValid = true;
  }
}

function submitForm() {
  validateForm();
  if (!formIsValid.value) {
    return;
  }
  emit("form-submitted");
}
</script>
