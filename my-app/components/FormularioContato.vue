<template>
    <form action="" @submit.prevent="receberDados">
        <label for="nome"> Nome: </label>
        <input type="text" v-model="inputNome" name="nome" id="nome">
        <label for="email"> Email: </label>
        <input type="text" v-model="inputEmail" name="email" id="email">
        <label for="msg"> Mensagem: </label>
        <textarea name="msg" v-model="inputMensagem" id="msg"> </textarea>

        <button>
            Enviar
        </button>
    </form>
</template>

<script>

export default {
    data() {
        return {
            inputNome: "",
            inputEmail: "",
            inputMensagem: ""
        }
    },
    methods: {
        receberDados() {
            const dados = {
                nome: this.inputNome,
                email: this.inputEmail,
                msg: this.inputMensagem,
            }
            this.$emit("enviarDados", dados)
        }
    }
}
</script>