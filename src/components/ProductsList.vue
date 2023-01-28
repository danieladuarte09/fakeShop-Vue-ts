<template>
    
      <div class="product-box" v-for="product in products" :key="product.id">
        <div>
          <img v-if="product.images[0]" :src="product.images[0]" alt="foto-producto">
        </div>


        <div class="product-name">
          <h2>{{ product.title }}</h2>
        </div>

        <div class="product-info">
          <p>${{ product.description }}</p>
          
        </div>

        <div class="product-price">
          <p>${{ product.price }}</p>
          
        </div>
        <button @click="viewDetails(product.id)">View Details</button>
      </div>
  </template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import fakeShopApi from "../api/fakeShopApi";
import {products} from"@/models/products";


export default defineComponent({
  data() {
    return {
      products: [] as products[],
    }
  },
  methods: {
    async getData() {
      try{
        const response = await fakeShopApi.get<products[]>('/products');
        this.products = response.data;
        console.log(this.products);
      } catch (error) {
        console.log(error);
      }
    },
    viewDetails(id: number) {
      this.$router.push({
        path: `/details${id}`
      })
    }
  },
  created() {
        this.getData();
  }
})
</script>

<style scoped>

img {
  width: 15em;
}
.product-box {
  display: inline-block;
  margin: 20px;
  width: 350px;
 
}
.product-info{
    
    text-align: justify;
    margin-left: 40px;
    margin-right: 40px;
    
}

</style>