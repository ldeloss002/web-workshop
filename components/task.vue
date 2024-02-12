<template>
  <div class="task" >
    <div class="task__checkbox" />
    <div class="task__content" />
    <div class="task__remove" />
  </div>
</template>

<style lang="scss">
.task {
  @apply flex gap-2 items-center p-2 rounded-md shadow-md;

  background-color: #ddd;

  &__checkbox {
    @apply w-4 h-4 rounded-md bg-white border-2 border-gray-400;
  }

  &__content {
    @apply flex-1 w-30 h-2 mr-8 rounded-md;

    background-color: #555;
  }

  &__remove {
    @apply w-12 h-6 rounded-md bg-red-500;
  }
}
</style>
