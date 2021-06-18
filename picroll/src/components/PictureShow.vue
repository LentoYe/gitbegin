<template>
  <div class="list">
    <ul>
      <li class="p1"><a href=""><img src="../assets/11.png" alt=""></a></li>
      <li class="p2"><a href=""><img src="../assets/22.png" alt=""></a></li>
      <li class="p3"><a href=""><img src="../assets/33.png" alt=""></a></li>
      <li class="p4"><a href=""><img src="../assets/44.jpg" alt=""></a></li>
      <li class="p5"><a href=""><img src="../assets/55.jpg" alt=""></a></li>
      <li class="p6"><a href=""><img src="../assets/66.jpg" alt=""></a></li>
      <li class="p7"><a href=""><img src="../assets/77.jpg" alt=""></a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "PictureShow",
  data() {
    return {
      pictures: ['p1','p2','p3','p4','p5','p6','p7'],
    }
  },
  methods: {
    preving () {

    },
    nexting () {

    }
  },
}
</script>

<style scoped>
.list {
  width: 1200px;
  height: 300px;
  overflow: hidden;
  position: absolute;
  left: 50%;
  margin-left: -600px;
}
li {
  list-style: none;
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0.5;
  transition: all 0.3s ease-out;
}
img {
  height: 300px;
  float: left;
}

.p1{
  transform:translate3d(-224px,0,0) scale(0.81);
}
.p2{
  transform:translate3d(0px,0,0) scale(0.81);
  transform-origin:0 50%;
  opacity: 0.8;
  z-index: 2;
}
.p3{
  transform:translate3d(224px,0,0) scale(1);
  z-index: 3;
  opacity: 1;
}
.p4{
  transform:translate3d(449px,0,0) scale(0.81);
  transform-origin:100% 50%;
  opacity: 0.8;
  z-index: 2;
}
.p5{
  transform:translate3d(672px,0,0) scale(0.81);
}
.p6{
  transform:translate3d(896px,0,0) scale(0.81);
}
.p7{
  transform:translate3d(1120px,0,0) scale(0.81);
}
</style>
