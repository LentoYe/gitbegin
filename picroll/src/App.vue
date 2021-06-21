<template>
  <div class="box">
    <picture-show></picture-show>


  </div>
</template>

<script>

import PictureShow from "./components/PictureShow";

export default {
  name: 'App',
  components: {
    PictureShow,

  },
  data() {
    return {
      isActive: false,
    }
  },
  methods: {
    bigChange () {
      this.isActive = !this.isActive;
    }

  }

}
</script>

<style>
.box {
  position: relative;
  width: 100%;
  height: 340px;
}
.active {
  color: orange;
  font-size: 40px;
}
</style>
