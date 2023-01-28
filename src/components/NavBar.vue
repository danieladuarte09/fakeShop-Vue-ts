<template>
    <nav>
        <div class="title">
            <h4>{{ title }}</h4>
        </div>

        <div class="links">  
            <router-link to="/">Home</router-link> |
            <router-link to="/products">Product List</router-link> |
            <router-link to="/perfil">Perfil</router-link>
        </div>

        <div class="logut">
            <button>Cerran sesión</button>
        </div>

    </nav>
  
    
    <router-view/>
  </template>