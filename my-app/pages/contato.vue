<template>
    <h1>
        Pagina de Contato
    </h1>

    <FormularioContato
        @enviarDados="receberDados"
    />
    <hr/>
    <h2>Lista de contatos: </h2>
    <ul v-for="ct in Object.keys(listaContato)">
        <li> Nome: <strong>{{ listaContato[ct].nome }}</strong></li>
        <li> email: <strong>{{ listaContato[ct].email }}</strong></li>
        <li> msg: <strong>{{ listaContato[ct].msg }}</strong></li>
        <hr />
    </ul>
</template>

<script>
export default {
    data() {
        return {
            listaContato: [
            ]
        }
    },
    methods: {
        receberDados(dados) {
            this.listaContato.push(dados)
        }
    }
}
</script>