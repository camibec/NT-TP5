<template>
  <div>
    <li v-for="(p, index) in productos" :key="index">
        ID: {{ p.id }} - {{p.desc}} - ${{p.precio}}
    </li>
    <br>
            Id <input v-model= "idIngresado">
            <br><br>
            Descripcion <input v-model= "descIngresado">
            <br><br>
            Precio <input v-model= "precioIngresado">
            <br><br>
    <br>
    <button v-on:click="agregar">Agregar Producto</button>        
  </div>
</template>

<script>
export default {
    name: 'lista',
    props: ['productos'],
    data() {
        return {
        idIngresado: '',
        descIngresado:'',
        precioIngresado:''
    } },
    methods: {
        agregar() {
            this.productos.push({id: this.idIngresado, desc: this.descIngresado, precio: this.precioIngresado})
        },
        modificar() {

        },
        eliminar() {

        }
    } 
}
</script>

<style>

</style>