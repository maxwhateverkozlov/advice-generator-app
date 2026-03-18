<script setup>
import { ref, onMounted } from 'vue';
import AdviceCard from './components/AdviceCard.vue';

const adviceId = ref(0);
const adviceText = ref("Loading...");

const fetchAdvice = async () => {
  try {
    const response = await fetch("https://api.adviceslip.com/advice");

    const data = await response.json();

    adviceId.value = data.slip.id;
    adviceText.value = data.slip.advice;
  } catch (error) {
    console.error("Error loading the advice:", error);
    adviceText.value = "Failed to load advice. Try again!";
  }
}
</script>

<template>
  <main class="bg-dark-blue min-h-screen flex justify-center items-center font-manrope">
    <AdviceCard
    :id="adviceId"
    :text="adviceText"
    @refresh="fetchAdvice"/>
  </main>
</template>
