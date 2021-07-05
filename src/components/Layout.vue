<template>
  <div class="layout">
    <div class="bottom-line"></div>
    <div class="bottom-area"></div>
    <img
      class="penguin1"
      src="../assets/penguin1.svg"
      alt="penguin1"
      width="50px"
      height="84px"
    />
    <img
      class="penguin2"
      src="../assets/penguin2.svg"
      alt="penguin2"
      width="50px"
      height="84px"
    />
  </div>
</template>

<script>
</script>

<style scoped lang="scss">
.layout {
  width: 100vw;
  height: 100vh;
  background-color: #2a4254;
}
.bottom-area {
  position: absolute;
  width: 100%;
  height: 223px;
  left: 0px;
  bottom: 0px;

  background: #c7e7ff;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
}
.bottom-line {
  position: absolute;
  width: 100%;
  height: 16px;
  left: 0px;
  bottom: 223px;

  background: #e9f5fe;
  transform: matrix(1, 0, 0, -1, 0, 0);
}
.penguin1 {
  position: absolute;
  width: 50.91px;
  height: 84px;
  left: 10%;
  bottom: 223px;
  transform: matrix(-1, 0, 0, 1, 0, 0);
}
.penguin2 {
  position: absolute;
  width: 49.64px;
  height: 84px;
  left: 5%;
  bottom: 223px;
  transform: matrix(-1, 0, 0, 1, 0, 0);
}
</style>