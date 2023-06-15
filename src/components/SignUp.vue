<template>
<img class="logo1" src="../assets/logo1.png">
<h1>Registracija</h1>
<div class="registracija">
    <input type="text" placeholder="Unesite ime" />
    <input type="email" placeholder="Unesite email" />
    <input type="password" placeholder="Unesite lozinku" />
    <button> Registriraj se </button>
</div>
</template>
<script>
export default {
    name :'SignUp'
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
    
}
</style>