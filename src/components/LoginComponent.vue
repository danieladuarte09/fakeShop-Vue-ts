<template>
  <div class="contenedor">
    <h1>Bienvenido</h1>

    <form id="loginForm">
      <input type="text" name="user" placeholder="Usuario" required>
      <input type="password" placeholder="Contraseña" name="password" required> 
      <Button type="submit" title="ingresar" name="ingresar">Iniciar sesión</Button>
    </form>

    <div class="footer-form">
      <a href="#">¿Olvidaste tu contraseña?</a>
      <a href="#">¿No tienes cuenta? Registrate</a>
    </div>
    
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Login-page',
  props: {
    msg: String,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

a {
  color: #42b983;
}

#loginForm, .footer-form{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 2px;
 
  margin: 5px;
}
input{
  margin: 5px;
}





</style>
