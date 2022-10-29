<script setup>
</script>

<template>
 <div class = "brand">
    <img class="logo" src="logo.svg" alt="logo"/>
    <h1 class = "title">Triviantastic</h1>
    <img class="logo" src="logo.svg" alt="logo"/>
 </div>

<div class="categories">
<RouterLink :to="`/question/category/${n}`" v-for="n in 24" :key="n" class="category">Category -{{n}}
</RouterLink>
</div>
  </template>


<style lang="postcss" scoped>
.brand {
    @apply flex items-center justify-center gap-4;

    & .logo{
        @apply h-16 w-16;
    }

    & .title{
        @apply text-5xl font-thin tracking-widest text-gray-800 uppercase;
    }
}

.categories{
    @apply grid flex-grow grid-cols-4 gap-12;

    & .category{
        @apply flex h-32 w-40 items-center justify-center rounded-lg border-4 border-blue-500 py-4 font-bold uppercase text-slate-600 transition-colors duration-300;

        &:hover {
            @apply cursor-pointer border-slate-700 bg-slate-700 text-white
        }
    }
}
</style>