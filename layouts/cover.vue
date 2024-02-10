<template>
  <div class="relative slidev-layout cover">
    <div class="absolute right-10 top-10 flex items-center jusfity-center gap-6 font-4xl font-bold bg-white text-black rounded-6 p-4" >

      <img src="/gwc.png" class="w-30" />

      +

      <img src="/ccny-acm.webp" class="w-30" />
    </div>


    <div class="my-auto w-full">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.cover {
  background-color: #7c57c5;
  color: white;
}
</style>
