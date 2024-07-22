<script setup>

defineProps(['dados', 'nomeEstados'])

</script>

<template>

    <div class="form">

        <h1>Edite o seu Perfil</h1>

        <form>

            <div>
                <label for="nome">Nome:</label>
                <input id="nome" type="text" v-model="dados.nome">
            </div>

            <div>
                <label for="email">Email:</label>
                <input id="email" type="email" v-model="dados.email">
            </div>

            <div>
                <label for="dataNasc">Data de Nascimento:</label>
                <input id="dataNasc" type="date" v-model="dataNasc.nome">
            </div>

            <div>
                <label for="cidade">Cidade:</label>
                <input id="cidade" type="text" v-model="cidade.nome">
            </div>

            <div>
                <label for="senha">Senha:</label>
                <input id="senha" type="password" v-model="dados.senha">
            </div>

            <div>
                <label for="cSenha">Confirmação de senha:</label>
                <input id="cSenha" type="password" v-model="cSenha.nome">
            </div>

        </form>

    </div>
  
</template>

<style scoped>

</style>