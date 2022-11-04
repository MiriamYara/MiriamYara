<template>
    <div>
         {{mensaje}}
         <br/>
         {{numero}}
         <br/>
         <label for="nombreempresa"></label>
         <input type="text" v-model="nombreempresa">{{nombreempresa}}
          <br/>
         <label for="ciudad"></label>
         <input type="text" v-model="ciudad">{{ciudad}}
         <br/>
         <label for="ventas"></label>
         <input type="text" v-model="ventas">{{ventas}}
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
         mensaje:"ubicacionEmpresas",
         numero:4,
         nombreempresa:null,
         ciudad:null,
         ventas:null,
        }
        

    },
    methods:{
        datos(){
          alert(this.nombreempresa+" "+this.ciudad+" "+this.ventas)  
        }
    }
}

