<template>
<div class="margin " >
  <el-carousel :interval="5000" arrow="always" height="450px"  style="width:100%">
    <el-carousel-item v-for="item in imgs" :key="item.index" >
        <div style="height:450px">
            <img :src="item.src" alt="" class="img">
        </div>
    </el-carousel-item>
  </el-carousel>
</div>
</template>

<script>
export default {
  data() {
    return {
      imgs: [
        { src: require("../../assets/img/bannner1.jpg"), index: 1 },
        { src: require("../../assets/img/bannner2.jpg"), index: 2 },
        { src: require("../../assets/img/bannner3.jpg"), index: 3 }
      ]
    };
  }
};
</script>

<style>
</style>
<style lang="scss" scoped>
@import "src/style/mixin";
.el-carousel__item img {
  display: block;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
.img {
  width: 100%;
  height: 100%;
}
.margin {
  p {
    text-align: center;
    margin-bottom: 20px;
    color: rgb(51, 51, 51);
    font: 18px/36px 微软雅黑;
    background: url(../../assets/img/slider3.jpg) center center no-repeat;
  }
}
</style>

