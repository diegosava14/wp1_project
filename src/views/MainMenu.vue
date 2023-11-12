<template>
  <html>
    <body>
      <header>
        <div class="actionButtons">
          <img class="back" src="./images/logout_FILL0_wght400_GRAD0_opsz24.svg"/>
          <img class="account" src="./images/account_circle_FILL0_wght400_GRAD0_opsz24.svg"/>
        </div>
        <div class="title">
          <h1>BATTLE<br>ARENA</h1>
        </div>
      </header>
        <main>
          <div class="buttons">
            <CustomButton type="button">PLAY</CustomButton>
            <CustomButton type="button">GAME FINDER</CustomButton>
            <CustomButton type="button">CREATE GAME</CustomButton>
            <CustomButton type="button">RANKING</CustomButton>
            <CustomButton type="button">STORE</CustomButton>
          </div>
        </main>
    </body>
  </html>
</template>

<script setup>
import CustomButton from './components/CustomButton.vue';
</script>

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
  rotate: 180deg;
}

.account {
  position: absolute;
  top: 0;
  right: 0;
  width: 30px;
  height: auto;
  margin-top: 10px;
  margin-right: 10px;
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

.buttons {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 20px;
}
</style>
