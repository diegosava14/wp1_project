<template>
  <html>
    <body>
      <header>
        <div class="title">
          <h1>BATTLE<br>ARENA</h1>
        </div>
      </header>
      <main>
        <div class="form">
          <TextInput id="username" placeholder="Username" v-model="username" />
          <TextInput id="password" placeholder="Password" v-model="password" />
        </div>
        <div class="buttons">
          <CustomButton type="button">JOIN</CustomButton>
          <CustomButton type="button">CREATE</CustomButton>
        </div>
      </main>
    </body>
  </html>
</template>

<script setup>
import CustomButton from './components/CustomButton.vue';
import TextInput from './components/TextInput.vue';

let username = '';
let password = '';
</script>

<style scoped>
html, body{
  margin:0;
  height: 100%;
}

body{
  background: #133973;
  position:absolute;
  top:0;
  right:0;
  bottom:0;
  left:0;
  height:100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 auto 30px;
}

.title h1 {
  color: #EBEF25;
  text-align: center;
  font-family: 'Porter Sans Block';
  font-size: 50px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 20px;
}

.title{
  margin-bottom: 60px;
  justify-content: center;
}

.form {
  margin-bottom: 30px;
}

.buttons {
  align-items: center;
}
</style>