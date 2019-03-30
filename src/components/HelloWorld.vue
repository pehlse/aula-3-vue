<template>
  <div class="hello">
    <label>Deixe sua mensagem aqui</label>
    <p v-if="visibleIf">Testando o v-if</p>
    <p v-show="visibleShow">Testando o v-show</p>
    <div style="margin-top: 10px;">
      <input type="text" v-model="message.text">
      <button @click="mostrarMensagem" >Mostrar mensagem</button>
    </div>
    <button @click="exibeParagrafos" style="margin: 10px 0;">Exibir os parágrafos</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      visibleIf: false,
      visibleShow: false,
      message: {
        text: '',
        title: '',
      },
    };
  },
  methods: {
    mostrarMensagem() {
      alert('aqui sua mensagem ' + this.message.text);
    },

    exibeParagrafos() {
      this.visibleIf = true;
      this.visibleShow = true;
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
