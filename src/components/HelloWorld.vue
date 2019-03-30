<template>
  <div class="hello">
    <label>Deixei sua mensagem aqui</label>
    <div style="margin-top: 10px;">
      {{ arrayOfObjects[0].message }}<br>
      <input type="text" v-model="message.text">
      <button @click="mostrarMensagem" >Mostrar mensagem</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      arrayOfObjects: [{
        message: 'mensagem 1',
        number: 1,
      }, {
        message: 'mensagem 1',
        number: 2,
      }],
      message: {
        text: '',
        title: '',
      },
    };
  },
  methods: {
    mostrarMensagem() {
      alert('aqui sua mensagem ' + this.message.text);
    }
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
