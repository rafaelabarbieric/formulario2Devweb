<script setup>

defineProps(['dados'])

import { ref } from 'vue'

let estados = [
  {name: 'AC'},
  {name: 'AL'},
  {name: 'AP'}, 
  {name: 'AM'}, 
  {name: 'BA'}, 
  {name: 'CE'}, 
  {name: 'DF'},
  {name: 'ES'}, 
  {name: 'GO'}, 
  {name: 'MA'}, 
  {name: 'MT'}, 
  {name: 'MS'}, 
  {name: 'MG'}, 
  {name: 'PA'}, 
  {name: 'PB'}, 
  {name: 'PR'}, 
  {name: 'PE'}, 
  {name: 'PI'}, 
  {name: 'RJ'}, 
  {name: 'RN'},
  {name: 'RS'}, 
  {name: 'RO'}, 
  {name: 'RR'}, 
  {name: 'SC'}, 
  {name: 'SP'}, 
  {name: 'SE'},
  {name: 'TO'}
  ]

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
                <input id="dataNasc" type="date" v-model="dados.dataNasc">
            </div>

            <div>
                <label for="endereco">Endereço</label>
                <input id="endereco" type="text" v-model="dados.endereco">
            </div>

            <div>
                <label for="cidade">Cidade:</label>
                <input id="cidade" type="text" v-model="dados.cidade">
            </div>

            <div>
                <label for="estado">Estado:</label>
                <select name="estados" id="estado" v-model="dados.estados">
                    <option v-for="estado of estados " :key="estado" value="estado.name">{{ estado.name }}</option>
                </select>
            </div>

            <div>
                <label for="hobbies">Hobbies:</label>
                <input type="checkbox" v-model="dados.hobbies" id="esportes" value="esportes"> Esportes
                <input type="checkbox" v-model="dados.hobbies" id="musica" value="musicas"> Músicas
                <input type="checkbox" v-model="dados.hobbies" id="filme" value="filmes"> Filmes
                <input type="checkbox" v-model="dados.hobbies" id="viagens" value="viagens"> Viagens
                <input type="checkbox" v-model="dados.hobbies" id="leitura" value="leitura"> Leitura
            </div>

            <div>
                <label for="senha">Senha:</label>
                <input id="senha" type="password" v-model="dados.senha">
            </div>

            <div>
                <label for="cSenha">Confirmação de senha:</label>
                <input id="cSenha" type="password" v-model="dados.cSenha">
            </div>

        </form>


    </div>
  
</template>

<style scoped>

</style>