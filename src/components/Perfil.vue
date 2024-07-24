<script setup>

defineProps(['dadosPerfil'])

</script>

<template>

<div class="container">
    <div class="perfil">
        <section>
            <h1 style="text-align: center;">{{ dadosPerfil.nome }}</h1>
        </section>

            <section class="blocoDados">
                <p>Email: {{ dadosPerfil.email }}</p>
                <p>Senha: {{ dadosPerfil.senha }}</p>
                <p>Data de nascimento: {{ dadosPerfil.dataNasc }}</p>
                <p>Endereço: {{ dadosPerfil.endereco }}, {{ dadosPerfil.cidade }} - {{ dadosPerfil.estados }}</p>
                <p>Hobbies: {{ dadosPerfil.hobbies }}</p>
                <p>Linguagem favorita de programação: {{ dadosPerfil.lingProg }}</p>
                <p>Biografia: {{ dadosPerfil.biografia }}</p>
            </section>    
    </div>
</div>

</template>

<style scoped>

.container{
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 5%;
    background-color: #655BA6;

}
.perfil{
    height: 60%;
    width: 25%;
    border: 2px solid black;
    border-radius: 10px;
    padding: 10px;
}

.blocoDados{
    margin-left: 5%;
}
</style>