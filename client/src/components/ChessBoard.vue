<template>
  <div class="flex flex-col items-center mt-10">
    <h2 class="text-2xl font-bold mb-4"> Chess Board</h2>
    <div class="grid grid-cols-8 w-80 h-80 border-4 border-gray-700">
      <div
        v-for="square in 64"
        :key="square"
        :class="[
          'flex items-center justify-center text-lg font-bold select-none',
          (Math.floor((square - 1) / 8) + square) % 2 === 0
            ? 'bg-amber-200'
            : 'bg-amber-800 text-white'
        ]"
      >
        {{ square }}
      </div>
    </div>
  </div>
</template>

<script setup>
</script>
