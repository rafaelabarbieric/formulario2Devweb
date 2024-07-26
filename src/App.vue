<script setup>

//#655BA6 color

import { reactive, ref, computed } from 'vue'
import Formulario from '@/components/Formulario.vue'
import Perfil from '@/components/Perfil.vue'

const user = reactive([
  {nome: ''},
  {email: ''},
  {senha: ''},
  {cSenha: ''},
  {dataNasc: ''},
  {endereco: ''},
  {cidade: ''},
  {estados: ''},
  {hobbies: []},
  {lingProg: ''},
  {biografia: ''},
])

const button = ref(false)
function enviar() {
  if (user.senha == user.cSenha) {
    button.value = true
  }
}
function voltar() {
  button.value = false
}
</script>

<template>
  
  <Formulario v-if="!button" :dados="user" @enviar = "enviar()"></Formulario>

  <Perfil v-if="button" :dados-perfil="user" @voltar="voltar()"></Perfil>

</template>

<style scoped>

</style>
