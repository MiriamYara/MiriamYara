<template>
    <div>
         {{mensaje}}
         <br/>
         {{numero}}
         <br/>
         <label for="nombreproducto"></label>
         <input type="text" v-model="nombreproducto">{{nombreproducto}}
          <br/>
         <label for="precio"></label>
         <input type="text" v-model="precio">{{precio}}
         <br/>
         <label for="referencia"></label>
         <input type="text" v-model="referencia">{{referencia}}
         <br/>
         <label for="garantia"></label>
         <input type="text" v-model="garantia">{{garantia}}
         <br/>

         <button v-on:click="datos">Acaptar</button> 
          
    </div>
</template>
<script>
import Siderbar from '../components/Siderbar.vue';
export default{
    name:"Vmodel",
    props:{

    },
    data(){
        return{
         mensaje:"productos",
         numero:3,
         nombreproducto:null,
         precio:null,
         referencia:null,
         garantia:null,
        }
        

    },
    methods:{
        datos(){
          alert(this.nombreproducto+" "+this.precio+" "+this.referencia+" "+this.garantia)  
        }
    },
    components:{
        Siderbar
    }
}


</script>
