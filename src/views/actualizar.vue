<template>
    <div>
        <label>userId</label>
        <input type="text" v-model="form.userId"/>
        <label >id</label>
        <input type="text" v-model="form.id"/>
        <label >title</label>
        <input type="text" v-model="form.title"/>
        <label >title</label>
        <input type="text" v-model="form.body"/>
        <button @click="actualizar(form.userid)">Guardar</button>
        <button @click="cancelar()">Cancelar</button>
    </div>
</template>
<script>
import axios from "axios"
export default {
    data(){
        return{
            form: {
                userid: null,
                id: null,
                title: null,
                body:null,
            }

        }
    },
    methods: {
        async actualizar(id){
            await axios.put("https://jsonplaceholder.typicode.com/posts/"+id,this.form).then(response =>{
                console.log(response)
                this.router.push("/Ejemplo2")
        });
        },
        cancelar(){

        }

    },
    computed:{

    },
    async mounted() {
        let id = this.$route.params.id
        await axios.get("https://jsonplaceholder.typicode.com/posts/1"+id).then(response =>{
        this.form.userid = responde.data.userId
        this.form.id = response.data.id
        this.form.title = response.title
        this.form.body = response.data.body
        });
    }
}
</script>