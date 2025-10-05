<template>
  <div class="container">
    <h1>🌳 Recreation Park Portal</h1>
    <button @click="fetchHello">Call Backend</button>
    <p v-if="message">{{ message }}</p>
    <p v-if="error" style="color: red;">⚠️ {{ error }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const message = ref('');
const error = ref('');

const fetchHello = async () => {
  try {
    const response = await fetch('http://localhost:8080/api/hello');
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    message.value = await response.text();
    error.value = '';
  } catch (err) {
    error.value = 'Error calling backend 😢';
    console.error('Fetch error:', err);
  }
};
</script>

<style>
.container {
  max-width: 600px;
  margin: 4rem auto;
  text-align: center;
  font-family: Arial, sans-serif;
}

button {
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  background-color: #4CAF50;
  border: none;
  border-radius: 5px;
  color: white;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}
</style>
