<script setup>

</script>

<template>
<main>
  <div class ="card">
  <RouterView />
  </div>
</main>
  <p class = "score">Score: 100</p>
</template>


<style lang = "postcss" scoped>
  main {
    @apply flex justify-center items-center h-screen bg-gradient-to-br from-gray-400 via-gray-600 to-blue-800;

    & .card {
      @apply flex h-5/6 min-h-fit w-11/12 flex-col items-center gap-16 overflow-auto rounded-lg bg-white p-8 shadow-lg;
    }
  }

  .score {
    @apply absolute bottom-0 right-0 m-8 text-2xl font-bold text-white uppercase;
}
</style>