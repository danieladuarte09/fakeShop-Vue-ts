<template>
  <div class="products">
    <h1>Products</h1>
  </div>

  <products-list/>
  
</template>

<script lang="ts">

import { defineComponent } from 'vue';
import ProductsList from '@/components/ProductsList.vue';

export default defineComponent({
  name: 'ProductsView',
  components:{
    ProductsList
  }
})

</script>
