<template>
  <body>
      <lista 
            :productos="[{ id: '011', desc: 'Papas', precio: '150' },
                { id: '012', desc: 'Sprite', precio: '80' },
                { id: '013', desc: 'Hamburguesa', precio: '300' },
                { id: '014', desc: 'Pancho', precio: '200' }]"> </lista>
  </body>
</template>


<script>
import Lista from './Lista.vue'

export default {
    name: 'cuerpo',
    components: {
        Lista,
    },
    

}
</script>

<style>

</style>