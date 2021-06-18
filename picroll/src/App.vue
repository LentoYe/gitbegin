<template>
  <div class="box">
    <picture-show></picture-show>
    <slide-button></slide-button>
    <bottom-button></bottom-button>
  </div>
</template>

<script>
import SlideButton from './components/SlideButton.vue'
import BottomButton from "./components/BottomButton";
import PictureShow from "./components/PictureShow";

export default {
  name: 'App',
  components: {
    PictureShow,
    BottomButton,
    SlideButton
  }

}
</script>

<style>
.box {
  position: relative;
  width: 100%;
  height: 340px;
}
</style>
