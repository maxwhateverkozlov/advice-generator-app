<script setup>
import DiceButton from './DiceButton.vue';

defineProps({
  id: Number,
  text: String
});

</script>

<template>
  <div class="bg-dark-grayish-blue rounded-2xl p-8 max-w-md w-full text-center shadow-2xl relative">
      <p class="text-neon-green font-extralight mb-8 text-[11px] uppercase ">Advice #{{ id }}</p>
      <blockquote class="text-light-cyan">"{{ text }}"</blockquote>
      <div class="my-8">
        <img src="/pattern-divider-mobile.svg" 
      alt="divider"
      class="block md:hidden w-full">
      <img src="/pattern-divider-desktop.svg" 
      alt="divider"
      class="hidden md:block w-full">
      </div>
        <DiceButton @click="$emit('refresh')" />
    </div>
</template>