<template>
  <table class='grid'>
    <tr>
      <cell name='1'></cell>
      <cell name='2'></cell>
      <cell name='3'></cell>
    </tr>
    <tr>
      <cell name='4'></cell>
      <cell name='5'></cell>
      <cell name='6'></cell>
    </tr>
    <tr>
      <cell name='7'></cell>
      <cell name='8'></cell>
      <cell name='9'></cell>
    </tr>
  </table>
</template>

<script>
export default {
  data() {
    return {
      activePlayer: 'x', 
      gameStatus: 'turn', //can be: turn, win, or draw
      gameStatusMessage: "X's turn", 
      /*
        * status color is used as a background color in the status bar
        * statusTurn: yellow (default);
        * statusWin: green;
        * statusDraw: purple;
      */
      gameStatusColor: 'statusTurn', 
      moves: 0, 
      //cells stores the placement of x's and 0's in cells by their cell number
      cells: {
        1: '', 2:'', 3:'', 
        4: '', 5: '', 6: '', 
        7: '', 8: '', 9: ''
      },

    }
  }
};
</script>

<style>
.grid {
  background-color: #34495e;
  color: #fff;
  width: 100%;
  border-collapse: collapse;
}

.gameStatus {
  margin: 0px;
  padding: 15px;
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  background-color: #f1c40f;
  color: #fff;
  font-size: 1.4em;
  font-weight: bold;
}

.statusTurn {
  background-color: #f1c40f;
}

.statusWin {
  background-color: #2ecc71;
}

.statusDraw {
  background-color: #9b59b6;
}
</style>
