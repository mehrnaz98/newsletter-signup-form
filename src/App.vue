<template>
  <main class="flex min-h-screen justify-center items-center bg-[#36384D]">
    <div class="bg-white rounded-3xl p-[3rem] flex flex-row">
      <picture class="responsive-image">
        <source media="(min-width: 768px)" srcset="desktop-image.jpg" />
        <img src="mobile-image.jpg" alt="Newsletter promotion" />
      </picture>
      <div>
        <h1 class="text-[3rem]">Stay updated!</h1>
        <p class="text-[1rem]">
          Join 60,000+ product managers receiving monthly updates on:
        </p>
        <ul class="custom-list">
          <li>Product discovery and building what matters</li>
          <li>Measuring to ensure updates are a success</li>
          <li>And much more!</li>
        </ul>
        <form class="flex flex-col max-w-[6rem]">
          <label for="email">Email address</label>
          <input type="email" id="email" placeholder="email@company.com" />
          <button class="bg-[#232742]">Subscribe to monthly newsletter</button>
        </form>
      </div>
    </div>
  </main>
</template>

<script></script>
