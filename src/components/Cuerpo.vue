<template>
  <body>
      <lista> </lista>
  </body>
</template>


<script>
import Lista from './Lista.vue'

export default {
    props: ['index'],
    name: 'cuerpo',
    components: {
        Lista,
    },
    methods: {
        agregar() {
            this.productos.push({id: this.idIngresado, desc: this.descIngresado, precio: this.precioIngresado})
        },
        eliminar(index) {
            this.productos.splice(index, 1)
        }
    }
}
</script>

<style>

</style>