<template>
    <div>
         {{mensaje}}
         <br/>
         {{numero}}
         <br/>
         <label for="nombre"></label>
         <input type="text" v-model="nombre">{{nombre}}
          <br/>
         <label for="apellido"></label>
         <input type="text" v-model="apellido">{{apellido}}
         <br/>
         <label for="sexo"></label>
         <input type="text" v-model="sexo">{{sexo}}
         <br/>
         <label for="documento"></label>
         <input type="text" v-model="documento">{{documento}}
         <br/>
         <label for="cargo"></label>
         <input type="text" v-model="cargo">{{cargo}}
         <br/>

         <button v-on:click="datos">Aceptar</button>

    </div>
</template>
<script>
export default{
    name:"Vfor.vue",
    props:{

    },
    data(){
        return{
         mensaje:"Empleado",
         numero:1,
         nombre:null,
         apellido:null,
         sexo:null,
         documento:null,
         cargo:null
        }
        

    },
    methods:{
        datos(){
          alert(this.nombre+" "+this.apellido+" "+this.documento+" "+this.cargo)  
        }
    }
}


</script>
