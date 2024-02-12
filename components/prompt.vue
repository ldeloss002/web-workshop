<script setup lang="ts">
defineProps<{ addClass?: string | object }>();
</script>

<template>
  <div class="prompt" >
    <div class="prompt__input" />
    <div :class="['prompt__add', addClass]" />
  </div>
</template>

<style lang="scss">
.prompt {
  @apply flex gap-2 w-50 mb-4 items-center;

  &__input {
    @apply flex-1 h-7 rounded-md border-2 border-gray-400;

    background-color: #fff;
  }

  &__add {
    @apply w-10 h-6 rounded-md;

    background-color: #55d;
  }
}
</style>
