<script setup>
const items = [];
let i;

for (i = 0; i < 100; i++) {
  items.push({
    id: i,
    text: {
      attack: 'Attack ' + i,
      power: 'Power --> ' + 1,
      equipped: 'Equipped --> YES',
      onSale: 'On Sale --> NO'
    }
  });
}
</script>

<template>
  <html>
    <body>
      <header>
        <div class="actionButtons">
          <img class="back" src="./images/arrow_back_FILL0_wght400_GRAD0_opsz24.svg"/>
        </div>
        <div class="title">
          <h1>BACKPACK</h1>
        </div>
      </header>
      <main>
        <div class="scroll-list">
          <div v-for="item in items" :key="item.id" class="item-container">
            <a href="#">
              <p class="item-name">{{ item.text.attack }}</p>
              <p class="item-power">{{ item.text.power }}</p>
              <p class="item-equipped">{{ item.text.equipped }}</p>
              <p class="item-sale">{{ item.text.onSale }}</p>
            </a>
          </div>
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

.title h1 {
  color: #EBEF25;
  text-align: center;
  font-family: 'Porter Sans Block';
  font-size: 50px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 40px;
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

.title{
  margin-top: 20px;
  justify-content: center;
}

.scroll-list {
  background-color: #133973;
  overflow-y: auto;
  white-space: nowrap;
  max-height: 600px;
}

.scroll-list a {
  display: block;
  color: black;
  text-align: left;
  padding: 10px;
  text-decoration: none;
  background: #EBEF25;
  width: 250px;
  border-radius: 15px;
}

.scroll-list a:last-child {
  border-bottom: none;
}

.item-container {
  margin-bottom: 6px;
}

.item-name {
  font-weight: bold;
  color: steelblue;
  font-size: 1.2em;
}
</style>