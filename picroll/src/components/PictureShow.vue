<template>
  <div class="list" @mouseover="stopTiming" @mouseleave="beginTiming">
    <ul>
      <li v-for="(imgUrl,index) in imgUrls"
          :key="index"
          :class="pictures[index]"
          @click="ClickPic(index)"><img :src="imgUrl"></li>
    </ul>
  </div>

  <div class="slideBtu">
    <div @click="preving" class="left btn">&lt;</div>
    <div @click="nexting" class="right btn">></div>
  </div>

  <div class="botBtn">
    <span v-for="n in 7"
          :key="n"
          :class="{turnBlue:picIndex===n}"
          @click="ClickBtn(n)"
    ></span>
  </div>
</template>

<script>

export default {
  name: "PictureShow",
  components: {},
  data() {
    return {
      pictures: ['p0', 'p1', 'p2', 'p3', 'p4', 'p5', 'p6'],
      timer: '',
      picIndex: 2,
      imgUrls: [
        require("../assets/11.png"),
        require("../assets/22.png"),
        require("../assets/33.png"),
        require("../assets/44.jpg"),
        require("../assets/55.jpg"),
        require("../assets/66.jpg"),
        require("../assets/77.jpg"),
      ],
    }
  },
  // mounted() {
  //   this.timer = setInterval(this.nexting, 2000);
  // },
  methods: {
    nexting() {
      this.pictures.unshift(this.pictures[6]);
      this.pictures.pop();
      this.picIndex++;
      if (this.picIndex > 7) this.picIndex = 1;
    },
    preving() {
      this.pictures.push(this.pictures[0]);
      this.pictures.shift();
      this.picIndex--;
      if (this.picIndex <= 0) this.picIndex = 7;
    },
    ClickBtn (n) {
      if(n-this.picIndex > 0){
        let m = n-this.picIndex;
        for(let i = 0; i < m; i++) this.nexting();

      } else {
        let m = this.picIndex-n;
        for(let i = 0; i < m; i++) this.preving();

      }
    },
    ClickPic (n) {
      if(this.picIndex===6 && n === 0) {
        this.nexting();
      } else if (this.picIndex===7 && n === 1){
        this.nexting();
      } else if (n > this.picIndex) this.nexting();
      else if(n < this.picIndex) this.preving();
    },
    // stopTiming () {
    //   clearInterval(this.timer);
    // },
    // beginTiming () {
    //   this.timer = setInterval(this.nexting, 2000);
    // },
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

.p0 {
  transform: translate3d(-224px, 0, 0) scale(0.81);
}

.p1 {
  transform: translate3d(0px, 0, 0) scale(0.81);
  transform-origin: 0 50%;
  opacity: 0.8;
  z-index: 2;
}

.p2 {
  transform: translate3d(224px, 0, 0) scale(1);
  z-index: 3;
  opacity: 1;
}

.p3 {
  transform: translate3d(449px, 0, 0) scale(0.81);
  transform-origin: 100% 50%;
  opacity: 0.8;
  z-index: 2;
}

.p4 {
  transform: translate3d(672px, 0, 0) scale(0.81);
}

.p5 {
  transform: translate3d(896px, 0, 0) scale(0.81);
}

.p6 {
  transform: translate3d(1120px, 0, 0) scale(0.81);
}

.btn {
  position: absolute;
  top: 50%;
  font-size: 90px;
  color: white;
  background: rgba(0, 255, 0, 0.5);
  text-decoration: none;
  text-align: center;
  cursor: pointer;
}

.left {
  left: 0;
}

.right {
  right: 0;
}

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

.botBtn span {
  display: inline-block;
  width: 36px;
  height: 6px;
  margin: 0 3px;
}

span {
  display: block;
  background: red;
}

.turnBlue {
  background: blue;
}
</style>
