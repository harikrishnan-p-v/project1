<template>
  <div>
    <!-- Header section -->
    <header class="bg-white sticky top-0 flex pt-4 pb-5 px-5 gap-5 justify-between items-end shadow-lg z-10">
      <div class="flex items-end gap-3">
        <img src="public/img/wff_logo.jpg" alt="wff_logo" class="h-11 lg:h-16">
        <p class="font-bold text-sm lg:text-3xl font-roboto">Mr.&Ms South India 2025</p>
      </div>
      <NuxtLink v-if="getRoute === '/'" to="/register"
        class="bg-[#26A69A] text-white p-2 text-center lg:p-2 rounded-lg font-semibold cursor-pointer text-[12px] lg:text-[16px] lg:hover:text-[16.2px]">
        Register Now
      </NuxtLink>
      <NuxtLink v-else to="/"
        class="bg-[#26A69A] text-white p-2 text-center lg:p-2 rounded-lg font-semibold cursor-pointer text-[12px] lg:text-[16px] lg:hover:text-[16.2px]">
        Home
      </NuxtLink>
    </header>
    <!-- Main section -->
    <main>
      <slot />
    </main>
    <!-- <footer class="bg-white h-96">

    </footer> -->
  </div>
</template>

<script setup lang="ts">
const getRoute = computed(() => {
  return useRoute().path;
}
);
</script>