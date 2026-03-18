<script setup>
const emit = defineEmits(['click'])
</script>

<template>
  <button @click="emit('click')" class="absolute -bottom-8 left-1/2 -translate-x-1/2 bg-neon-green p-5 rounded-full hover:shadow-[0_0_40px_rgba(82,255,168,0.8)] transition-all duration-300 group cursor-pointer">
        <img src="/icon-dice.svg" alt="dice" class="w-6 h-6 group-hover:rotate-180 transition-transform duration-500">
      </button>
</template>