<template>
  <div>
    <header class="bg-indigo-300 py-4 px-2 font-serif">
      <h1 class="text-2xl text-center">My beautiful Webpage</h1>
      <div class="flex justify-around mt-4">
        <NuxtLink
          class="border-b-2 border-yellow-600 hover:text-yellow-600"
          to="/"
          >Home page</NuxtLink
        >
        <NuxtLink
          class="border-b-2 border-yellow-600 hover:text-yellow-600"
          to="/about/"
          >About</NuxtLink
        >
        <NuxtLink
          class="border-b-2 border-yellow-600 hover:text-yellow-600"
          to="/blog/"
          >Blog</NuxtLink
        >
        <NuxtLink
          class="border-b-2 border-yellow-600 hover:text-yellow-600"
          to="/promises/"
          >Promises</NuxtLink
        >
      </div>
    </header>
    <main class="py-4 px-2 font-sans">
      <Nuxt />
    </main>
  </div>
</template>

<script>
export default {
  head: {
    htmlAttrs: {
      class: "text-gray-900 leading-tight",
    },
    bodyAttrs: {
      class: "min-h-screen bg-gray-300",
    },
  },
};
</script>

<style>
</style>