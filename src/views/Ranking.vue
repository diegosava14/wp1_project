<script setup>
const items = [
  { id: 1, text: 'Item 1' },
  { id: 2, text: 'Item 2' },
];

const handleItemClick = (item) => {
  console.log('Item clicked:', item.text);
};
</script>

<template>
  <html>
    <body>
      <div class="container">
        <div class="actionButtons">
          <img class="back" src="./images/arrow_back_FILL0_wght400_GRAD0_opsz24.svg"/>
        </div>
        <div class="title">
          <h1>RANKING</h1>
        </div>
        <div class="scrollable-list">
          <ul>
            <li v-for="item in items" :key="item.id" @click="handleItemClick(item)">{{ item.text }}</li>
          </ul>
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

.scroll-list {
  height: 200px;
  overflow-y: auto;
  border: 1px solid #ccc;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

li {
  padding: 10px;
  border-bottom: 1px solid #eee;
  cursor: pointer;
}
</style>