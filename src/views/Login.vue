<template>
  <div class="container">
    <div class="login">
      <div class="title">Refeitório Admin</div>
      <div class="body">
        <label for="id_usuario">Usuário:</label>
        <input type="text" id="id_usuario" v-model="usuario">
        <label for="id_usuario">Senha:</label>
        <input type="password" id="id_usuario" v-model="senha">
      </div>
      <div class="submit-form">
          <input type="button" value="Acessar" @click="logar">
        </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "home",
  components: {},
  data() {
    return {
      credenciais: {
        user: 'admin',
        password: '1234'
      },
      usuario: '',
      senha: ''
    }
  },
  methods: {
    logar(){
      if(this.usuario == this.credenciais.user && this.senha == this.credenciais.password){
        this.$router.push({'name': 'home'});
      }
      else{
        alert('Usuário inválido');
      }
    }
  }
};
</script>
<style scoped>
    .container{ 
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      height: 80vh;
    }
   .login{
      width: 400px;
      height: 300px;
      background-color: #fff;
      border-radius: 5px 5px 0 0;
    }
    .login .title{
      text-align: center;
      border-radius: 5px 5px 0 0;
      color: rgba(255, 255, 255, 1);
      font-size: 15px;
      height: 35px;
      font-weight: 500;
      padding-top: 16px;
      background: #3f946c;
    }
    .login .body{
      padding: 20px;
    }
    .body label{
      display: block;
      padding-right: 0.5em;
      line-height: 2em;
      font-size: 14px;
      clear: both;
      color: #333;
    }
    .body input[type=text], .body input[type=password]{
      clear: both;
      padding: 8px;
      width: 100%;
      -webkit-box-sizing: border-box;
      -moz-box-sizing: border-box;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
      margin-bottom: 10px;
    }
    .submit-form{
      clear: both;
      padding: 1em 0 0 9.4em;
      margin: 0;
      border: none;
      background: none;
      text-align: left;
    }
    input[type=button]{
      background: #79c899;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      color: #fff;
      cursor: pointer;
    }
    input[type=button]:hover{
      background: #206750;
    }
</style>
