<script setup>

import { ref } from 'vue'
import Formulario from '@/components/Formulario.vue'
import Perfil from '@/components/Perfil.vue'

const user = ref([
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
  
  <Formulario :dados="user" :nome-estados="estados"></Formulario>

  <Perfil :dados-perfil="user"></Perfil>

</template>

<style scoped>

</style>
