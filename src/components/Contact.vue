<template>
  <div class="contact">
    <h1>{{ msg }}</h1>
    <p>You can reach me via email: <strong>contact@renam.com.br</strong></p>
    <h3>Why not send a whatsApp?</h3>
    <p>+55 15 99605.4066</p>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data () {
    return {
      msg: 'Contact me'
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
