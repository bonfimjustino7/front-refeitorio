<template>
    <div class="menu">
        <ul>
          <li><router-link to="/">Início</router-link></li>
          <li><router-link to="/login"> Sair</router-link></li>
        </ul>
     </div>
</template>
<script>
    
</script>
<style>
    * {
    padding: 0;
    margin: 0;
    }
    .menu{
    height: 50px;
    background: rgb(15, 173, 107);
    }
    .menu ul{
    padding: 15px;
    list-style: none;
    display: flex;
    justify-content: space-between;
    }
</style>