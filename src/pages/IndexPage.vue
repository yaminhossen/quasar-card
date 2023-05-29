<template>
  
    
    
      <div>
        <products></products>
      </div>
    
  
</template>

<script>
import { defineComponent } from 'vue'
import Products from 'src/components/Products.vue';

export default defineComponent({
  name: 'IndexPage',
  components: {
    Products
  }
})
</script>
