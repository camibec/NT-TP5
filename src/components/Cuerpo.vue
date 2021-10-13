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
}
</script>

<style>

</style>