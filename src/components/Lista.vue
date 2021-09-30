<template>
  <div>
    <li v-for="(p, index) in productos" :key="index">
        ID: {{ p.id }} - {{p.desc}} - ${{p.precio}}
            <button @click = "$emit('eliminar(index)')">Eliminar producto</button>
            <button v-on:click="modificar">Modificar</button>
            <button v-on:click="eliminar">Eliminar</button> 
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
        modificar(index) {
            let obj = this.productos[index]
                 
                    
                    obj.desc = this.descIngresado
                    obj.precio = this.precioIngresado
        },
        eliminar(index) {
            this.productos.splice(index, 1)
        }
    } 
}
</script>

<style>

</style>