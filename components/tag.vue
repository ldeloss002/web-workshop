<script setup lang="ts">
defineProps<{ name: string }>();

const colors = ['bg-red', 'bg-green', 'bg-blue', 'bg-purple', 'bg-yellow', 'bg-indigo', 'bg-pink'];
const bg = colors[Math.floor(Math.random() * colors.length)];
</script>

<template>
  <div :class="['b-3', 'gap-2', 'p-2', 'b-gray', 'flex', 'flex-col', bg, 'bg-op-20', 'rounded-3']">
    <span class="p-2 font-mono font-bold">{{ name }}</span>

    <slot />
  </div>
</template>
