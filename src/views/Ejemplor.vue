<template>
    <div>
        <siderbar></siderbar>
        {{numero}}
        <br/>
        {{mensaje}}
        <br/>
        {{valor}}
        <br/>
        <label for=nombre></label>
        <input type="text" v-model="nombre">{{nombre}}
        <br/>
        <label for=apellido></label>
        <input type="text" v-model="apellido">{{apellido}}
        <br/>
        <label for=direccion></label>
        <input type="text" v-model="direccion">{{direccion}}
        <br/>
        <label for=telefono></label>
        <input type="text" v-model="telefono">{{telefono}}
        <br/>
        <button v-on:click="datos">Aceptar</button>
    </div>
</template>
<script>
import Siderbar from '../components/Siderbar.vue'
export default{
    name:"Ejemplor",
    props:{

    },
    data(){
        return{
            numero:2,
            mensaje:"hola",
            valor:null,
            nombre:"Miriam ",
            apellido: null,
            direccion:null,
            telefono:null
            
        }

    },
    methods: {
        datos(){
            alert(this.nombre+" "+this.apellido+" "+this.direccion+" "+this.telefono)
        }
    },
    components:{
        Siderbar
    }
}
</script>

