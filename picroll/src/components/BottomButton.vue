<template>
  <div class="botBtn">
    <span v-for="n in 7"
          :key="n"
          :class="{turnBlue:isBlue[n]}"
          @click="changeColor(n)"></span>
  </div>

</template>

<script>
import isBlue from "./PictureShow";
export default {
  name: "BottomButton",

  data() {
    return {


    }
  },

  methods: {
    changeColor (m) {
      isBlue[m] = true;
    },

  }
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
.botBtn span{
  display: inline-block;
  width: 36px;
  height: 6px;
  margin: 0 3px;
}
span {
  display: block;
  background: red;
}
div>span:first-child, .turnBlue{
  background: blue;
}
</style>
