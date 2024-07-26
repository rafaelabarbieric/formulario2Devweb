<script setup>

defineProps(['dadosPerfil'])

</script>

<template>


    <div class="container">

        <div>
            <section id="nome">
                <h1 style="text-align: center;"><strong>{{ dadosPerfil.nome }}</strong></h1>
            </section>

            <h2>Informações pessoais</h2>
        </div>

        <hr>

    </div>

    <div>

            <section class="blocoDados">
                <p>Email: <strong>{{ dadosPerfil.email }}</strong></p>
                <p>Senha: <strong>{{ dadosPerfil.senha }}</strong></p>
                <p>Data de nascimento: <strong>{{ dadosPerfil.dataNasc }}</strong></p>
                <p>Endereço: <strong>{{ dadosPerfil.endereco }}, {{ dadosPerfil.cidade }} - {{ dadosPerfil.estados }}</strong></p>
                <p>Hobbies: <strong>{{ dadosPerfil.hobbies.join(', ') }}</strong></p>
                <p>Linguagem favorita de programação: <strong>{{ dadosPerfil.lingProg }}</strong></p>
                <p>Biografia: <strong>{{ dadosPerfil.biografia }}</strong></p>
            </section>    

            <section id="button">
                <input class="btn btn-outline-dark" @click="$emit('voltar')" type="button" value="Voltar">
            </section>

    </div>


</template>

<style scoped>

.container{
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 5%;
}

#nome{
    margin-bottom: 20%;
}

hr{
    width: 60%;
}
.blocoDados{
    display: inline-block;
    text-align: left;
    margin-left: 25%;
}

#button{
    text-align: center;
}
</style>