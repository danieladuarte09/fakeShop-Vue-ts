<template>
  <nav>
    <div class="links">  
    <router-link to="/">Home</router-link> |
    <router-link to="/products">Product List</router-link> |
    <router-link to="/perfil">Perfil</router-link>
  </div>
  </nav>

  
  <router-view/>
</template>

<script lang="ts">
import { defineComponent } from 'vue'


export default defineComponent({
  name: 'AppComponents',
  components:{
    
  }
 
})
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
  background: #2c3e50;
}

nav a {
  font-weight: bold;
  color: white;
}

nav a.router-link-exact-active {
  color:  white;
}

</style>
