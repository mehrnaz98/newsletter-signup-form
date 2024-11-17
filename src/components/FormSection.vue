<template>
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
    <form class="flex flex-col">
      <label for="email" class="roboto-bold text-[0.7rem] mt-7"
        >Email address</label
      >
      <input
        type="email"
        id="email"
        class="mt-2 border border-[#B3B2B7] text-[0.8rem] p-3 rounded-md"
        placeholder="email@company.com"
      />
      <button class="bg-[#232742] text-white mt-4 text-[0.8rem] p-3 rounded-md">
        Subscribe to monthly newsletter
      </button>
    </form>
  </div>
</template>
