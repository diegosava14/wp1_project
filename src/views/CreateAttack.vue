<script setup>

import CustomButton from "./components/CustomButton.vue";
import TextInput from "./components/TextInput.vue";

let name = "";
let xCoord = "";
let yCoord = "";
</script>

<template>
  <html>
    <body>
      <header>
        <div class="title">
          <img class="back" src="./images/arrow_back_FILL0_wght400_GRAD0_opsz24.svg"/>
          <h1>CREATE<br>ATTACK</h1>
        </div>
      </header>
      <main>
        <div class="form">
          <TextInput id="name" placeholder="Name" v-model="name" />
          <TextInput id="xCoord" placeholder="X" v-model="xCoord" />
          <TextInput id="yCoord" placeholder="Y" v-model="yCoord" />
        </div>
        <div class="buttons">
          <CustomButton type="button">CREATE</CustomButton>
        </div>
      </main>
    </body>
  </html>
</template>

<style scoped>
html, body{
  margin:0;
  height: 100%;
}

body {
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

.back {
  position: absolute;
  top: 0;
  left: 0;
  width: 30px;
  height: auto;
  margin-top: 10px;
  margin-left: 10px;
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
  margin-bottom: 30px;
  justify-content: center;
}

.form {
  margin-bottom: 30px;
}

.buttons {
  align-items: center;
}
</style>