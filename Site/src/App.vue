<script setup>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import HelloWorld from './components/HelloWorld.vue'
import LoginPage from './components/LoginPage.vue'
import LandPage from './components/LandPage.vue'

</script>

<template >
<div class="container p-5">
  <LoginPage v-if="!loggedIn"/>
  <LandPage v-else-if="loggedIn"/>
</div>
</template>



<script>
export default{
    data() {
        return {
            showMe: "",
            loggedIn: false
        };
    },
    components() {
        LoginPage,
        LandPage,
        FontAwesomeIcon;
    }
}
</script>


