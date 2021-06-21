<template>
  <div class="slideBtu">
    <div @click="preving" class="left btn">&lt;</div>
    <div @click="nexting" class="right btn">></div>
  </div>
</template>

<script>
export default {
  name: 'SlideButton',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.btn{
  position: absolute;
  top: 50%;
  font-size: 90px;
  color: white;
  background: rgba(0,255,0,0.5);
  text-decoration: none;
  text-align: center;
  cursor: pointer;
}

.left{
  left: 0;
}
.right {
  right: 0;
}
</style>
