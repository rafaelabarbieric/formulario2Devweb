<script setup>
import { ref } from 'vue'

const dados = ref(
  {
    nome: '',
    email: '',
    senha: '',
    cSenha: '',
    dataNasc: '',
    endereco: '',
    cidade: '',
    estados: '',
    hobbies: [],
    lingProg: '',
    biografia: ''
  }
)

let estados = [
    { name: 'AC' },
    { name: 'AL' },
    { name: 'AP' },
    { name: 'AM' },
    { name: 'BA' },
    { name: 'CE' },
    { name: 'DF' },
    { name: 'ES' },
    { name: 'GO' },
    { name: 'MA' },
    { name: 'MT' },
    { name: 'MS' },
    { name: 'MG' },
    { name: 'PA' },
    { name: 'PB' },
    { name: 'PR' },
    { name: 'PE' },
    { name: 'PI' },
    { name: 'RJ' },
    { name: 'RN' },
    { name: 'RS' },
    { name: 'RO' },
    { name: 'RR' },
    { name: 'SC' },
    { name: 'SP' },
    { name: 'SE' },
    { name: 'TO' }
]
</script>

<template>
    <div class="form">
        <form @submit.prevent="$emit('enviar', {...dados})">
            <div class="elements">
                <h2>Edite o seu Perfil:</h2>
            </div>

            <div action="/action_page.php" class="was-validated elements">
                <label class="form-label" for="nome">Nome:</label>
                <input 
                    class="form-control" 
                    id="nome" 
                    type="text" 
                    v-model="dados.nome" 
                    required 
                />
                <div class="valid-feedback">Valido</div>
                <div class="invalid-feedback">Campo Obrigátorio</div>
            </div>

            <div action="/action_page.php" class="was-validated elements">
                <label class="form-label" for="email">Email:</label>
                <input 
                    class="form-control" 
                    id="email" type="email" 
                    v-model="dados.email" 
                    required
                />
                <div class="valid-feedback">Valido</div>
                <div class="invalid-feedback">Campo Obrigátorio</div>
            </div>

            <div class="elements">
                <label class="form-label" for="dataNasc">Data de Nascimento:</label>
                <input 
                    class="form-control" 
                    id="dataNasc" 
                    type="date" 
                    v-model="dados.dataNasc" 
                />
            </div>

            <div class="elements">
                <label class="form-label" for="endereco">Endereço</label>
                <input 
                    class="form-control" 
                    id="endereco" 
                    type="text" 
                    v-model="dados.endereco" 
                />
            </div>

            <div class="elements">
                <label class="form-label" for="cidade">Cidade:</label>
                <input
                    class="form-control" 
                    id="cidade" 
                    type="text" 
                    v-model="dados.cidade" 
                />
            </div>

            <div class="elements">
                <label class="form-label" for="estado">Estado:</label>
                <select class="form-select" name="estados" id="estado" v-model="dados.estados">
                    <option v-for="estado of estados" :key="estado" :value="estado.name">
                        {{ estado.name }}
                    </option>
                </select>
            </div>

            <div class="elements">
                <label class="form-label">Hobbies:</label>
                <div class="form-check">
                    <input 
                        type="checkbox"
                        v-model="dados.hobbies" 
                        name="esportes" 
                        id="esportes" 
                        value="Esportes" 
                    /> Esportes
                </div>
                <div class="form-check">
                    <input 
                        type="checkbox" 
                        v-model="dados.hobbies" 
                        name="musica" 
                        id="musica" 
                        value="Musicas" 
                    /> Músicas
                </div>
                <div class="form-check">
                    <input 
                        type="checkbox" 
                        v-model="dados.hobbies" 
                        name="filme" 
                        id="filme" 
                        value="Filmes" 
                    /> Filmes
                </div>
                <div class="form-check">
                    <input 
                        type="checkbox" 
                        v-model="dados.hobbies" 
                        name="viagens" 
                        id="viagens" 
                        value="Viagens" 
                    /> Viagens
                </div>
                <div class="form-check">
                    <input 
                        type="checkbox" 
                        v-model="dados.hobbies" 
                        name="leitura" 
                        id="leitura" 
                        value="Leitura"
                    /> Leitura
                </div>
            </div>

            <div class="elements">
                <label class="form-label" for="lingProg">Sua Linguagem de Progamação Favorita:</label>
                <div class="form-check">
                    <input 
                        class="form-check-input" 
                        type="radio" 
                        v-model="dados.lingProg" 
                        value="C" 
                /> C
                </div>
                <div class="form-check">
                    <input 
                        class="form-check-input" 
                        type="radio" 
                        v-model="dados.lingProg" 
                        value="JavaSctipt" 
                    /> JavaScript
                </div>
                <div class="form-check">
                    <input 
                        class="form-check-input" 
                        type="radio" 
                        v-model="dados.lingProg" 
                        value="Python" 
                    /> Python
                </div>
            </div>

            <div class="elements">
                <label class="form-label" for="bio">Biografia:</label>
                <textarea class="form-control" type="text" id="bio" v-model="dados.biografia"></textarea>
            </div>

            <div></div>

            <div action="/action_page.php" class="was-validated elements">
                <label class="form-label" for="senha">Senha:</label>
                <input 
                    class="form-control" 
                    id="senha" 
                    type="password" 
                    v-model="dados.senha" 
                    required 
                />
                <div class="valid-feedback">Valido</div>
                <div class="invalid-feedback">Campo Obrigátorio</div>
            </div>

            <div action="/action_page.php" class="was-validated elements">
                <label class="form-label" for="cSenha">Confirmação de senha:</label>
                <input 
                    class="form-control" 
                    id="cSenha" 
                    type="password" 
                    v-model="dados.cSenha" 
                    required 
                />
                <div class="valid-feedback">Valido</div>
                <div class="invalid-feedback">Campo Obrigátorio</div>
            </div>

            <div class="elements">
                <input id="color-button" class="btn btn-outline-dark" type="submit" value="Enviar" />
            </div>
        </form>
    </div>
</template>

<style scoped>
.form {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 5%;
    margin-bottom: 5%;
}

form {
    border: 1px solid rgb(223, 219, 219);
    border-radius: 6px;
}

.elements {
    margin: 20px;
}

.margem-hobbies{
    margin-left: margem-hobbies;
}
</style>
