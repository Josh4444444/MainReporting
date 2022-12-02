<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from './components/HelloWorld.vue'

</script>

<template>

  <HelloWorld msg="Broadway Partners" />
  <div v-if="showMe == 'show'"> Hello! </div>
  <div v-else-if="!showMe"> Please Enter Your Password </div>
  <div v-else >Not Recognised</div>
  <input v-model="showMe">

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

<script>
export default{
  data () {
    return {
      showMe: ''
    }  
  }
};

</script>

