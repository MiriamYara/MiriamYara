<template>
    <div>
        <siderbar></siderbar>
         {{mensaje}}
         <br/>
         {{numero}}
         <br/>
         <label for="nombre"></label>
         <input type="text" v-model="nombre">{{nombre}}
          <br/>
         <label for="raza"></label>
         <input type="text" v-model="raza">{{raza}}
         <br/>
         <label for="años"></label>
         <input type="text" v-model="años">{{años}}
         <br/>
         <button v-on:click="datos">Aceptar</button>

    </div>
</template>
<script>
import Siderbar from '../components/Siderbar.vue';
import Navbar from '../components/Navbar.vue';
import Footer from '../components/Footer.vue';
export default{
    name:"Vfor",
    props:{

    },
    data(){
        return{
         mensaje:"Mascota",
         numero:1,
         nombre:null,
         raza:null,
         años:5
        }
        

    },
    methods:{
        datos(){
          alert(this.nombre+" "+this.raza+" "+this.años)  
        }
    },
    components:{
        Siderbar,
        Navbar,
        Footer
    }
}


</script>
