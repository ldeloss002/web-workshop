<template>
  <div class="box">
    <slot />
  </div>
</template>

<style>
.box {
  @apply text-center font-bold gap-4 items-center justify-center content-center justify-items-center p-10 border-3 rounded-3 w-60 h-60;
}
</style>
