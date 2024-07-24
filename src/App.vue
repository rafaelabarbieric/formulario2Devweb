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
const buttonName = computed(() =>
  button.value ? 'Voltar' : 'Enviar',
)

</script>

<template>
  
  <Formulario v-if="!button" :dados="user"></Formulario>

  <Perfil v-if="button" :dados-perfil="user" ></Perfil>

  <button @click="button=!button">{{buttonName}}</button>


</template>

<style scoped>

</style>
