<script setup>

//#655BA6 color

import { reactive } from 'vue'
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

</script>

<template>
  
  <Formulario :dados="user"></Formulario>

  <Perfil :dados="user"></Perfil>

</template>

<style scoped>

</style>
