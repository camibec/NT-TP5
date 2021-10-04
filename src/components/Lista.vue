<template>
  <div>
    <div class = "row">
        <div class= "col-6">Id<input v-model="id"></div>
    </div>
    <br>
    <div class = "row">
        <div class= "col-6">Descripción<input v-model="desc"></div>
    </div>
    <br>
    <div class = "row">
        <div class= "col-6">Precio<input v-model="precio"></div>
    </div>
    <br><br>

    <button v-on:click="agregar">Agregar</button>   
    <br>
    {{"Lista de Productos"}}
    <br><br>
    <li v-for="(p, index) in productos" :key="index">
        ID: {{ p.id }} - {{p.desc}} - ${{p.precio}}

            <button v-on:click="modificar(index)">Modificar</button>
            <button v-on:click="eliminar(index)">Eliminar</button> 
    </li>
    
        
  </div>
</template>

<script>
export default {
    name: 'lista',
    data() {
        return {
        id: '',
        desc:'',
        precio:'',
        productos: [{ id: '011', desc: 'Papas', precio: '150' },
                { id: '012', desc: 'Sprite', precio: '80' },
                { id: '013', desc: 'Hamburguesa', precio: '300' },
                { id: '014', desc: 'Pancho', precio: '200' }
            ]
        }
    },
    methods: {
        limpiar() {
            this.id = '',
            this.desc = '',
            this.precio = ''
        },
        agregar() {
            this.productos.push({id: this.id, desc: this.desc, precio: this.precio})
            this.limpiar();
        },
        modificar(index) {
            
            let obj = this.productos[index]
            if (obj != null){
                obj.desc = this.desc;
                obj.precio = this.precio;
            }
            this.limpiar();                  
                   
        },
        eliminar(index) {
            this.productos.splice(index, 1)
        }
    } 
}
</script>

<style>

</style>