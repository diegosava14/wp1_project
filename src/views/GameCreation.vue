<script setup>
import CustomButton from './components/CustomButton.vue';
import CustomLabel from './components/CustomLabel.vue';

let textArenaSize = 'Arena size';
let textPlayersHP = 'Player HP';
</script>

<template>
  <html>
  <body>
  <div class="container">
    <div class="actionButtons">
      <img class="back" src="./images/arrow_back_FILL0_wght400_GRAD0_opsz24.svg"/>
    </div>
    <div class="title">
      <h1>GAME<br>CREATION</h1>
    </div>
    <div class="content">
      <div class="labels">
        <div class="greenRectangle">
          <CustomLabel id="Arena's size" :labelText="textArenaSize"></CustomLabel>
          <select>
            <option value="Option1">2X2</option>
            <option value="Option2">3X3</option>
            <option value="Option3">4X4</option>
          </select>
        </div>
        <div class="greenRectangle">
          <CustomLabel id="Player's HP" :labelText="textPlayersHP"></CustomLabel>
          <select>
            <option value="Option1">10HP</option>
            <option value="Option2">25HP</option>
            <option value="Option3">50HP</option>
          </select>
        </div>
      </div>
      <div class="buttons">
        <CustomButton type="button">ENTER GAME</CustomButton>
      </div>
    </div>
  </div>
  </body>
  </html>
</template>

<style scoped>
html, body{
  margin:0;
  height: 100%;
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

.container {
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

.title{
  margin-top: 20px;
  justify-content: center;
}

select{
  margin-left: 5px;
  margin-right: 5px;
}

.labels{
  margin-bottom: 15px;
}

.buttons {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 10px;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.labelWithSelect {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 15px;
}

select {
  margin-left: 5px;
}

.greenRectangle {
  background-color: #EBEF25; /* Green color */
  padding: 10px; /* Adjust padding as needed */
  border-radius: 5px; /* Optional: Add rounded corners */
  margin-bottom: 15px; /* Add margin between pairs */
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>