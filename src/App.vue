<template>
  <div id="app">
    <h1>City: {{ weather.city }}</h1>
    <h2>Temperature: {{ weather.temperature }}°C</h2>
    <h3>Description: {{ weather.description }}</h3>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import axios from 'axios';

const weather = ref({ city: '', temperature: '', description: '' });

const fetchWeather = async () => {
  try {
    const response = await axios.get('http://127.0.0.1:5000/api/weather'); // 修正したエンドポイントを使う
    console.log(response.data);
    weather.value = response.data;
  } catch (error) {
    console.error('API エラー:', error);
  }
};

onMounted(fetchWeather);
</script>
