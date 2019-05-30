<template>
  <div class="product-form">
    <h2>{{ msg }}</h2>
    <button class='btn btn-success mt-5 mb-5'
        @click="addNewProductForm">
        Añadir nuevo
    </button>
    <div class='card mb-3'
      v-for='(product, index) in products' :key="index">
      <div class='card-body'>
        <span class='float-right' style='cursor:pointer'
            @click='deleteProductForm(index)'> X
        </span>
        <h4 class='card-title'>Producto #{{ index }}</h4>
        <div class='product-form'>
          <input type='text' class='form-control mb-2' placeholder='Nombre'
              v-model='product.name'>
          <input type='text' class='form-control mb-2' placeholder='Categoria'
              v-model='product.category'>
          <textarea cols='30' rows='10' class='form-control' placeholder='Descripción'
              v-model='product.description'></textarea>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductForm',
  template: 'product-form',
  props: {
    msg: String
  },
  data: () => {
    return {
      products: [{
        name: '',
        category: '',
        description: ''
      }]
    }
  },
  methods: {
    addNewProductForm() {
        this.products.push({
          name: '',
          category: '',
          description: ''
        })
    },
    deleteProductForm(index) {
      this.products.splice(index, 1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>