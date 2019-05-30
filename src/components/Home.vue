<template>
  <div>
    <ProductForm/>
    <sidebar-menu :menu="menu" :collapsed="true"/>
  </div>
</template>

<script>
import ProductForm from './ProductForm.vue'

import Vue from 'vue'
import VueSidebarMenu from 'vue-sidebar-menu'
import 'vue-sidebar-menu/dist/vue-sidebar-menu.css'

Vue.use(VueSidebarMenu)

export default {
  name: 'Home',
  template: 'home',
  components: { 
    ProductForm
  },
  props: {
    msg: String,
    collapsed: Boolean
  },
  data: () => {
    return {
      menu: [
        {
          header: true,
          title: 'Formularios'
        },
        {
          href: '/',
          title: 'Productos',
          icon: 'fa fa-book'
        }, {
          href: '#',
          title: 'Clientes',
          icon: 'fa fa-users'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>