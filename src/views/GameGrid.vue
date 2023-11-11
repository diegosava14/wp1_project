<template>
  <section>
    <nav>
      <button>&larr;</button>
      <time datetime="2023-07-11">7/11/23</time>
    </nav>
    <article>
      <table>
        <thead>
        <tr>
          <th scope="col" v-for="n in grid[0].length" :key="n"></th>
        </tr>
        </thead>
        <tbody>
        <tr v-for="(row, rowIndex) in grid" :key="rowIndex">
          <td v-for="(cell, cellIndex) in row" :key="cellIndex" :class="{ 'filled': cell }">
            <div v-if="players[0].position.x === cellIndex && players[0].position.y === rowIndex" class="player-circle green"></div>
            <div v-if="players[1].position.x === cellIndex && players[1].position.y === rowIndex" class="player-circle red"></div>
          </td>
        </tr>
        </tbody>
      </table>
    </article>
    <footer>
      <div class="players">
        <div class="player" v-for="player in players" :key="player.name">
          <h2>{{ player.name }}</h2>
          <progress :value="player.hp" max="30"></progress>
          <span>{{ player.hp }}/30HP</span>
          <ol>
            <li v-for="attack in player.attacks" :key="attack">{{ attack }}</li>
          </ol>
        </div>
      </div>
    </footer>
  </section>
</template>

<script>
export default {
  name: 'GameView',
  data() {
    return {
      grid: this.createGrid(10, 10), // Assuming a 10x10 grid for example
      players: [
        { name: 'MANOLITO', hp: 25, attacks: ['Fireball', 'Magic Shield', 'Pit of Doom'], position: { x: 1, y: 1 } }, // Position for player 1
        { name: 'PEPITO', hp: 10, attacks: ['Fireball', 'Magic Shield', 'Pit of Doom'], position: { x: 8, y: 8 } }, // Position for player 2
      ],
    };
  },
  methods: {
    createGrid(rows, cols) {
      return Array.from({ length: rows }, () => Array.from({ length: cols }, () => false));
    },
  },
};
</script>


<style scoped>


section {
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


nav {
  display: flex;
  justify-content: space-between;
  width: 90%;
}


table {
  border-collapse: collapse;
  width: 100%;
  max-width: 600px;
  margin: auto;
}


td {
  background-color: #D9D9D9;
  width: 20px;
  height: 20px;
  position: relative;
  border: 2px solid #000;
}


td::after {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #EBEF25;
  opacity: 0;
}


td.filled::after {
  opacity: 1;
}



.players {
  display: flex;
  justify-content: space-around;
  width: 100%;
}


.player {
  display: flex;
  flex-direction: column;
  align-items: center;
  flex-basis: 45%;
  margin: 0.5rem;
}



.player-circle {
  position: absolute;
  width: 70%;
  height: 70%;
  border-radius: 50%;
}

.green {
  background-color: #166D1A;
}

.red {
  background-color: #731313;
}

progress {
  width: 100%;
}
</style>

