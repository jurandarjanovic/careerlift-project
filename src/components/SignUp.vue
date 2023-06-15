<template>
<img class="logo1" src="../assets/logo1.png" title="CareerLift">
<h1>Registracija</h1>
<div class="registracija">
    <input type="text" v-model="name" placeholder="Unesite ime" />
    <input type="email" v-model="email" placeholder="Unesite email" />
    <input type="password" v-model="password" placeholder="Unesite lozinku" />
    <button v-on:click="signUp"> Registriraj se </button>
</div>
</template>
<script>
import axios from 'axios'
export default {
    name :'SignUp',
    data()
    {
        return {
            name:'',
            email:'',
            password:''
        }
    },
    methods:{
        async signUp()
        {
            let result = await axios.post("http://localhost:3000/korisnici",{
               email:this.email,
               password:this.password,
               name:this.name
            });

            console.warn(result);
            if(result.status==201)
            {
                alert("sign-up done");
                localStorage.setItem("user-info",JSON.stringify(result.data))
            }
        }
    }
}
</script>

<style>
.logo1{
    width: 150px;
}
.registracija input{
    width: 300px;
    height: 40px;
    padding-left: 20px;
    display: block;
    margin-bottom: 30px;
    margin-right: auto;
    margin-left: auto;
    border: 1px solid skyblue;
}
.registracija button{
    width: 320px;
    height: 40px;
    border: 1px solid skyblue;
    background: skyblue;
    color: white;
    cursor: pointer;

}
</style>