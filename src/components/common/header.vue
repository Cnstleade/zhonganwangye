<template>
    <div :class="{fix,}">
      <div class="top">
		        <div class="k1" >
              <span class="left" style="font-style:italic">
               <i>中安融资租赁欢迎您！</i> 
              </span>
		        	<a class="right ico2" href="javascript:void(0)"><router-link :to="'/login'">登录</router-link><i class="ico"></i></a>
              <span class="right">
                  &nbsp;/&nbsp;
              </span>
		        	<a class="right" href="javascript:void(0)" target="_blank"><router-link :to="'/register'">注册</router-link><i class="ico"></i></a>
		        </div>
	    </div>
        <el-row class="header" style="position:relative">
            <div class="k1 navbar clear margin">
	         	<a class="logo left" href="/" >
                  <img src="../../assets/img/img.jpg" alt="" height="100" style="height:100px" >
            </a>
	        	<ul class="right">
	        		<li><a href="javascript:void(0)" class="rhaver">首页</a>			
	        		</li>
	        		<li><a href="javascript:void(0)" @click="log('Business')">业务领域</a>
	        		</li>
	        		<li><a href="javascript:void(0) " @click="log('AboutUs')">关于我们</a>
	        		</li>
	        		<li><a href="javascript:void(0)" @click="log('IndustryNews')">行业资讯</a>
	        		</li>
	        		<li><a href="javascript:void(0)" @click="log('LawsRegulations')">法律法规</a>

	        		</li>
	        		<li><a href="javascript:void(0)" @click="log('JoinUs')">加入我们</a>
	        			<!-- <div class="sanjiao"></div>
	        			<div class="erji erji2" style="width: 360px;display: none;">
	        				<a href="Presence.aspx" style="background: none;">嘉德风采</a>
	        				<a href="JobSociology.aspx">社会招聘</a>
	        				<a href="JobCampus.aspx">校园招聘</a>
	        				<a href="Contact.aspx">联系方式</a>
	        			</div> -->
	        		</li>
              <li><a href="javascript:void(0)" @click="log('ContactWay')">联系我们</a>

              </li>
	        	</ul>
	         </div>
        </el-row>
    </div>
</template>

<script>
import bus from "./bus";
export default {
  data() {
    return {
      fix: false,
      man: true
    };
  },
  methods: {
    log(index) {
      bus.$emit("collapse", index);
    },
    handleScroll() {
      // var scrollTop =
      //   window.pageYOffset ||
      //   document.documentElement.scrollTop ||
      //   document.body.scrollTop;
      // if (scrollTop > 100) {
      //   this.fix = true;
      //   bus.$emit("collaps", this.fix);
      // } else {
      //   this.fix = false;
      //   bus.$emit("collaps", this.fix);
      // }
    }
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  }
};
</script>

<style>
.fix {
  position: fixed;
  background-color: #fff;
  top: 0;
  z-index: 999;
  width: 100%;
  margin: auto;
}
.header {
  height: 100px;
  background: #fff;
}
.k1 {
  width: 1100px;
  height: 100px;
}
</style>
<style lang="scss" scoped>
@import "src/style/mixin";
.top {
  width: 100%;
  height: 30px;
  background: #333;
  position: relative;
  .k1 {
    width: 1100px;
    margin: 0 auto;
  }
  a,span {
    font: 14px/30px "微软雅黑";
    color: #ccc;
    padding-right: 14px;
  }
}
.navbar {
  li {
    float: left;
    padding: 0 18px;
    position: relative;
    a {
      color: rgb(51, 51, 51);
      display: block;
      font: 16px/18px 微软雅黑;
      padding: 38.5px 15px;
    }
    .rhaver {
      color: #197c56;
    }
    div {
      position: absolute;
    }
  }
}
</style>

