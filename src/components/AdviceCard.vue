<script setup>
import DiceButton from './DiceButton.vue';

defineProps({
  id: Number,
  text: String
});

</script>

<template>
  <div class="bg-dark-grayish-blue rounded-2xl p-8 md:p-12 max-w-md md:max-w-[540px] w-full text-center shadow-2xl relative transition-all">
      <p class="text-neon-green font-extralight mb-8 text-[11px] uppercase ">Advice #{{ id }}</p>
      <blockquote class="text-light-cyan text-[24px] md:text-[28px]">"{{ text }}"</blockquote>
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