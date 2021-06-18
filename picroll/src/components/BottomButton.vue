<template>
  <div class="botBtn">
    <a href=""><span class="first"></span></a>
    <a href=""><span></span></a>
    <a href=""><span></span></a>
    <a href=""><span></span></a>
    <a href=""><span></span></a>
    <a href=""><span></span></a>
    <a href=""><span></span></a>
  </div>
</template>

<script>
export default {
  name: "BottomButton"
}
</script>

<style scoped>
.botBtn {
  width: 1200px;
  height: 30px;
  position: absolute;
  bottom: 0;
  left: 50%;
  color: orange;
  margin-left: -600px;
  text-align: center;
  padding-top: 10px;
}
.botBtn a{
  display: inline-block;
  width: 36px;
  height: 10px;
  margin: 0 3px;
}
span {
  display: block;
  width: 35px;
  height: 4px;
  background: red;
}
.first {
  background: blue;
}
</style>
