<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue'
</script>

<template>
    <div class="container">
      <Header title="Task Tracker"/>
    </div>

  <RouterView />
</template>

<script>
  export default {
    name: 'App',
    components: {
      Header,
    }
  }
</script>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');

  h1 {
      box-sizing: border-box;
      margin: 0;
      color: black;
    }
</style>