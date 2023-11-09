<template>
  <div class="container">
    <div class="title">
      <h1>BATTLE ARENA</h1>
    </div>
    <div class="form">
      <TextInput id="username" placeholder="Username" v-model="username" />
      <TextInput id="password" placeholder="Password" v-model="password" />
    </div>
    <div class="buttons">
      <CustomButton type="button">JOIN</CustomButton>
      <CustomButton type="button">CREATE</CustomButton>
    </div>
  </div>
</template>

<script setup>
import CustomButton from './components/CustomButton.vue';
import TextInput from './components/TextInput.vue';

let username = '';
let password = '';
</script>

<style scoped>
body, html {
  margin: 0;
  padding: 0;
  background: #133973;
}

.container {
  background: #133973;
  color: #fff;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.title h1 {
  color: #EBEF25;
  text-align: center;
  font-family: 'Porter Sans Block';
  font-size: 96px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.buttons {
  display: flex;
  justify-content: center;
}
</style>