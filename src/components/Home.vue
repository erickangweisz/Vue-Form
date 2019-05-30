<template>
  <div>
    <ProductForm msg="Formulario de Productos"/>
  </div>
</template>

<script>
import ProductForm from './ProductForm.vue'

export default {
  name: 'Home',
  template: 'home',
  components: { 
    ProductForm
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>