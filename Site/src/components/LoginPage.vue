<script setup>
import { ref } from 'vue'
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome"



</script>

<template>
    
<div id="Logging-Page">
<h1>Broadway Partners</h1>
<div id="userName">
<div>Username:</div>
<input v-model="user">
</div>
<div v-if="showMe === 'Tigger69'" style="color:green;"> Correct - Logging in now </div>
<div v-else-if="!showMe"> Password: </div>
<div v-else id="wrongPassword" style="color:red;">Not Recognised</div>
<input  v-model="showMe" type="password">
</div>
</template>

<script>
export default{
  data () {
    return {
      showMe: '',
      user: ''
    } 
  },

  }
</script>

