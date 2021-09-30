<template>
  <body>
      <lista v-on:eliminar(index)="eliminar(index)"
            :productos="[{ id: '011', desc: 'Papas', precio: '150' },
                { id: '012', desc: 'Sprite', precio: '80' },
                { id: '013', desc: 'Hamburguesa', precio: '300' },
                { id: '014', desc: 'Pancho', precio: '200' }]"> </lista>
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