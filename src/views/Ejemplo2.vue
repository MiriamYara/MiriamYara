<template>
<div>
    <navbar></navbar>
    <div class="content">
    <table >
        <thead>
            <tr>
                <th>userId</th>
                <th>id</th>
                <th>titulo</th>
                <th>body</th>
                <th>Acciones</th>
            </tr>
        </thead>
        <tbody>  
            <tr v-for="posts in posts" :key="posts.id">
               <td> {{posts.userId}} </td>
                <td> {{posts.id}} </td>
                <td>{{posts.title}}</td>
                <td>{{posts.body}}</td>
                <td><button @click="actualizar(posts.id)">actualizar</button></td>
                <td><button @click="eliminar(posts.id)">eliminar</button></td>
            </tr>
            
        </tbody>

        <button class="botoncancelar">cancelar</button>    
    </table>
    </div>
    <Footer class="contentfooter"></Footer>
</div>
</template>
<style >

.ContenidoFooter{
   display:flexbox;
   margin-top: 100px;
}
</style>
<script>
import Siderbar from '../components/Siderbar.vue'
import Navbar from '../components/Navbar.vue'
import Footer from '../components/Footer.vue'
import axios from 'axios'
export default{
   data(){
      return{
         posts:null
      }
   },
   methods:{
      actualizar(id){
            this.$router.push("/actualizar/"+id)
         },
      async eliminar(id){
         await axios.delete("https://jsonplaceholder.typicode.com/posts/"+id).then(response=>{

      })
      }

   },
   computed:{

   },
   components:{
      Siderbar,
      Navbar,
      Footer

   },
   async mounted(){
      axios.get("https://jsonplaceholder.typicode.com/posts").then(response=>{
            console.log(response.data)
            this.posts=response.data
        })
   },
}
</script>
