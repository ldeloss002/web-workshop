<script setup lang="ts">
defineProps<{
  checkboxClass?: string | object,
  contentClass?: string | object,
  removeClass?: string | object
  }>();
</script>

<template>
  <div class="task" >
    <div :class="['task__checkbox', checkboxClass]" />
    <div :class="['task__content', contentClass]" />
    <div :class="['task__remove', removeClass]" />
  </div>
</template>

<style lang="scss">
.task {
  @apply flex gap-2 w-70 items-center p-2 rounded-md shadow-md;

  background-color: #ddd;

  &__checkbox {
    @apply w-4 h-4 rounded-md bg-white border-2 border-gray-400;
  }

  &__content {
    @apply flex-1 h-2 mr-8 rounded-md transition-opacity;

    background-color: #555;
  }

  &__remove {
    @apply w-12 h-6 rounded-md;

    background-color: #d55;
  }
}
</style>
