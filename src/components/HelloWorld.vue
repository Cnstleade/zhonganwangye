<template>
  <div>
    <v-header></v-header>
    <v-slider></v-slider>
    <v-section></v-section>
    <v-footer></v-footer>
    <v-aside class="fixed"></v-aside>
  </div>
</template>

<script>
import vHeader from "@/components/common/header.vue";
import vSlider from "@/components/common/slider.vue";
import vFooter from "@/components/common/footer.vue";
import vSection from "@/components/common/section.vue";
import vAside from "@/components/common/aside.vue";

export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  },
  components: {
    vHeader,
    vFooter,
    vSlider,
    vSection,
    vAside
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.fixed{
 z-index: 99999;
}
.fixedbox {
  position: fixed;
  top: 300px;
  right: 50px;
  width: 83px;
  z-index: 99999;
}
</style>
