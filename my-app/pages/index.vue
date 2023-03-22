<template>
  <div>
    <p>
      Pagina Inicial
    </p>
    <h1>
      Lista
    </h1>

    <form action="" @submit.prevent="receberDados">
      <input type="text" v-model="inputName" name="name" id="" />

      <button> Adicionar </button>
    </form>

    <ul>
      <li v-for="name in names">{{ name }}</li>
    </ul>

  </div>
</template>

<script>

export default {
  data() {
    return {
      names: [],
      inputName: ""
    }
  },
  methods: {
    receberDados() {
      this.names.push(this.inputName)

    }
  }
}

</script>
