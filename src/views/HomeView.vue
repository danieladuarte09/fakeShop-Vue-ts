<template>
  <h1>Login-page</h1>
  <login-component/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import LoginComponent from '../components/LoginComponent.vue';

export default defineComponent({
  name: 'HomeView',
  components: {
   
   LoginComponent
  },
});
</script>
