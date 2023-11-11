<script setup>
import TextInput from "./components/TextInput.vue";
import CustomButton from "./components/CustomButton.vue";

let username = "";
let password = "";
</script>
<template>
  <html>
    <body>
      <header>
        <div class="title">
          <h1>CREATE<br>ACCOUNT</h1>
        </div>
      </header>
      <main>
        <div class="image">
          <img class="account_image" src="./images/account_circle_FILL0_wght400_GRAD0_opsz24.svg"/>
        </div>
        <div class="form">
          <TextInput id="username" placeholder="Username" v-model="username" />
          <TextInput id="password" placeholder="Password" v-model="password" />
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

.image {
  margin-bottom: 30px;
}

.account_image{
  width: 150px;
  height: 150px;
  filter: invert(100%) grayscale(100%);
}

.form {
  margin-bottom: 30px;
}

.buttons {
  align-items: center;
}
</style>