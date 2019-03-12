<template>
    <div class="fixedbox">
    	<a href="javascript:void(0)" class="aa1"  @click="log('Business')"></a>
    	<a href="javascript:void(0)" class="aa2" @click="log('AboutUs')"></a>
    	<a href="javascript:void(0)" class="aa3" @click="log('IndustryNews')"></a>
    	<a href="javascript:void(0)" class="aa4" @click="log('JoinUs')"></a>
    </div>
</template>

<script>
import bus from "./bus";
export default {
  data() {
    return {};
  },
  methods: {
    log(index) {
      bus.$emit("collapse", index);
    }
  }
};
</script>

<style scoped>
.fixedbox {
  position: fixed;
  top: 300px;
  right: 50px;
  width: 83px;
  z-index: 99999;
}
a {
  display: block;
  width: 83px;
  height: 83px;
  margin-bottom: 2px;
  opacity: 0.9;
  filter: Alpha(opacity=90);
  background-image: url(../../assets/img/fixed.jpg);
}
.aa1 {
  background-position: 0 0;
}
.aa2 {
  background-position: 0 -85px;
}
.aa3 {
  background-position: 0 -170px;
}
.aa4 {
  background-position: 0 -255px;
}
</style>

