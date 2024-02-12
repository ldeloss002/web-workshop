<template>
  <div class="slidev-layout two-cols">
      <slot />
  </div>
</template>

<style>
.slidev-layout.two-cols {
  @apply flex gap-4 items-center justify-around;
}
</style>
