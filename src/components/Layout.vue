<template>
  <div class="layout">
    <div class="board">
      <div class="board-col"></div>
      <div class="board-col">
        <div class="card"></div>
        <div class="card"></div>
        <div class="card"></div>
        <div class="card"></div>
        <div class="card"></div>
        <div class="card"></div>
        <div class="card"></div>
      </div>
      <div class="board-col"></div>
      <div class="board-col"></div>
      <div class="board-col"></div>
      <div class="board-col"></div>
      <div class="board-col"></div>
      <div class="board-col"></div>
    </div>
    <div class="store-div">
      <div class="store-col">
        <div class="card">1</div>
        <div class="card">2</div>
        <div class="card">3</div>
        <div class="card">4</div>
      </div>
      <div class="store-col">
        <div class="card">1</div>
        <div class="card">2</div>
        <div class="card">3</div>
        <div class="card">4</div>
      </div>
      <div class="store-col"></div>
      <div class="store-col"></div>
    </div>
    <div class="actions-div"></div>
    <div class="completed-div">
      <div class="completed-col">
        <div class="card">1</div>
        <div class="card">2</div>
        <div class="card">3</div>
        <div class="card">4</div>
      </div>
      <div class="completed-col"></div>
      <div class="completed-col"></div>
      <div class="completed-col"></div>
    </div>
  </div>
</template>

<script>
</script>

<style scoped lang="scss">
.layout {
  width: 100vw;
  height: 100vh;
  background-color: #2a4254;
  background-image: url(../assets/background-Start.svg);
  background-repeat: no-repeat;
  background-size: 100% auto;

  background-position: center;
  display: grid;
  grid-template-columns: 45% 10% 45%;
  grid-template-rows: auto $card-height;
  padding: 40px 70px;
}

.board {
  grid-column: 1 / 4;
  grid-row: 1 / 2;
}
.store-div {
  display: flex;
}
.store-col {
  @include card-container;
  border: 3px solid #fafafa;
  margin: 0 auto;
  position: relative;
}
.completed-div {
  display: flex;
}
.completed-col {
  @include card-container;
  border: 3px solid #fafafa;
  position: relative;
  background: rgba(255, 255, 255, 0.25);
  box-shadow: 0px -2px 4px rgba(0, 0, 0, 0.25);
  margin: 0 auto;

  &::before {
    content: "A";
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    font-family: Noto Sans;
    font-weight: 900;
    font-size: 60px;
    line-height: 109px;
    text-align: center;
    opacity: 0.2;
    color: #282828;
  }
}
.board {
  display: flex;
}
.board-col {
  @include card-container;
  border: 3px solid #fafafa;
  margin: 0 auto;
  position: relative;
}
.card {
  display: inline-block;
  height: $card-height;
  width: $card-width;
  background-image: url("../assets/card/Card_club 2.svg");
  background-repeat: no-repeat;
  position: absolute;
  top: -3px;
  left: -3px;
  background-color: white;
  border-radius: 15px;
  box-shadow: 0px -2px 4px rgba(0, 0, 0, 0.25);

  @for $i from 1 through 7 {
    .board-col > &:nth-child(#{$i}) {
      top: calc(#{$card-height}* 0.25 * (#{$i} - 1) + -3px);
    }
  }
}
</style>