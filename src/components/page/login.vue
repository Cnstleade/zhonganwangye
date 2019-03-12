<template>
    <div>   
                <div class="header">
            <div class="container">
                <!-- <div class="row">
                    <div class="logo span4">
                     
                        
                    </div>
     
                </div> -->
                <div class="k1">
                    <el-row>
                      <el-col :span="3">
                        <img src="../../assets/img/img.jpg" alt="" style="height:97px;"  >
                      </el-col>
                      <el-col :span="6">
                        <h1 style="margin-top:30px;margin-left:10px;  padding-left: 50px;color: #555;

                            font-size: 36px;
                            font-weight: 400;"><a href="" style="color:#e63c3c">登录 中安 <span class="red">.</span></a></h1>
                                                </el-col>
                                                <el-col :span="12">
                                                    <div class="links span8" style="margin-top:20px;">
                                                             <a class="home" href="" rel="tooltip" data-placement="bottom" data-original-title="Home" @click="go('/')" ></a>
                                                             <span style="position: relative;
                              top: -10px;">首页</span>
                                                             <a class="blog" href="javascript:void(0)" rel="tooltip" data-placement="bottom" data-original-title="Blog" @click="go('/register')"></a>
                                                             <span style="position: relative;
                              top: -10px;">注册</span>
                           </div>
                      </el-col>
                    </el-row>
                </div>
            </div>
        </div>
        <div class="register-container container">
            <div class="row">
                <div class="iphone span5">
                    <img src="../../assets/img/i.jpg" alt="" style="width:400px;height:600px">
                </div>
                <div class="register span6">
                    <form action="" method="post">
                        <h2>登录 <span class="red"><strong>中安</strong></span></h2>
                        <label for="firstname">账户</label>
                        <input type="text" id="firstname" name="firstname" placeholder="请输入您的账户">
                        <label for="password">密码</label>
                        <input type="password" id="password" name="password" placeholder="请输入您的密码">
                        <button @click.prevent="s">登录</button>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import vHeader from "@/components/common/header.vue";
export default {
  data() {
    return {};
  },
  components: {
    vHeader
  },
  methods: {
    go(t) {
      this.$router.push(t);
    },
    s() {}
  }
};
</script>

<style scoped>
@import "../../style/boots.css";
.k1 {
  width: 1100px;
  margin: 0 atuo;
}

strong {
  font-weight: 700;
}
.red {
  color: #eb4141;
}
a:hover {
  text-decoration: none;
}

.header {
  margin: 0 auto;
  padding-bottom: 5px;
  background: #fff url(../../assets/img/pattern.jpg) left top repeat;
  border-top: 3px solid #eb4141;
  -moz-box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.3);
  -webkit-box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.3);
  box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.3);
}

.logo h1 {
  padding-left: 50px;
  font-family: "Oleo Script", cursive;
  font-size: 36px;
  font-weight: 400;
}

.logo h1 a {
  color: #555;
}

.links {
  text-align: right;
}

.links a {
  display: inline-block;
  width: 30px;
  height: 30px;
  margin: 15px 0 0 20px;
}

.links a.home {
  background: url(../../assets/img//home.png) center center no-repeat;
}
.links a.blog {
  background: url(../../assets/img//blog.png) center center no-repeat;
}

.register-container {
  margin-top: 50px;
}

/* ----- iPhone ----- */

.iphone {
  text-align: right;
}

.iphone img {
  margin-right: 10px;
}

/* ----- Registration Form ----- */

.register form {
  padding: 20px 50px 40px 50px;
  background: #f8f8f8 url(../../assets/img//pattern.jpg) left top repeat;
  -moz-border-radius: 8px;
  -webkit-border-radius: 8px;
  border-radius: 8px;
  -moz-box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.3);
  -webkit-box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.3);
  box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.3);
  text-align: center;
}

.register form h2 {
  margin-bottom: 25px;
  padding-bottom: 15px;
  background: url(../../assets/img/pencil.png) 70px 6px no-repeat;
  border-bottom: 2px dotted #bbb;
  font-size: 30px;
  font-weight: 400;
  text-align: center;
}

.register form input {
  width: 95%;
  height: 30px;
  background: #fcfcfc;
  border: 1px solid #ddd;
  -moz-border-radius: 2px;
  -webkit-border-radius: 2px;
  border-radius: 2px;
  -moz-box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1) inset;
  -webkit-box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1) inset;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1) inset;
  font-family: "PT Sans", Helvetica, Arial, sans-serif;
  color: #888;
  font-size: 16px;
}

.register form input:focus {
  border: 1px solid #ccc;
  -moz-box-shadow: none;
  -webkit-box-shadow: none;
  box-shadow: none;
}

.register form label {
  margin: 7px 0 10px 5px;
  font-size: 16px;
  text-align: left;
}

.register form label span {
  font-style: italic;
}

.register form input:-moz-placeholder {
  color: #aaa;
}
.register form input:-ms-input-placeholder {
  color: #aaa;
}
.register form input::-webkit-input-placeholder {
  color: #aaa;
}

.register form button {
  cursor: pointer;
  width: 60%;
  height: 42px;
  margin-top: 25px;
  padding: 0;
  background: #eb4141;
  -moz-border-radius: 3px;
  -webkit-border-radius: 3px;
  border-radius: 3px;
  border: 0;
  -moz-box-shadow: 0 15px 30px 0 rgba(255, 255, 255, 0.1) inset;
  -webkit-box-shadow: 0 15px 30px 0 rgba(255, 255, 255, 0.1) inset;
  box-shadow: 0 15px 30px 0 rgba(255, 255, 255, 0.1) inset;
  font-family: "PT Sans", Helvetica, Arial, sans-serif;
  font-size: 16px;
  font-weight: 400;
  color: #fff;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
  -o-transition: all 0.2s;
  -moz-transition: all 0.2s;
  -webkit-transition: all 0.2s;
  -ms-transition: all 0.2s;
}

.register form button:hover {
  -moz-box-shadow: 0 -15px 30px 0 rgba(255, 255, 255, 0.05) inset;
  -webkit-box-shadow: 0 -15px 30px 0 rgba(255, 255, 255, 0.05) inset;
  box-shadow: 0 -15px 30px 0 rgba(255, 255, 255, 0.05) inset;
}

.register form button:active {
  -moz-box-shadow: 0 -15px 30px 0 rgba(255, 255, 255, 0.05) inset,
    0 5px 8px 0 rgba(0, 0, 0, 0.1) inset;
  -webkit-box-shadow: 0 -15px 30px 0 rgba(255, 255, 255, 0.05) inset,
    0 5px 8px 0 rgba(0, 0, 0, 0.1) inset;
  box-shadow: 0 -15px 30px 0 rgba(255, 255, 255, 0.05) inset,
    0 5px 8px 0 rgba(0, 0, 0, 0.1) inset;
}

.copyrights {
  text-indent: -9999px;
  height: 0;
  line-height: 0;
  font-size: 0;
  overflow: hidden;
}
/* ----- Media queries ----- */

@media (max-width: 1200px) {
  .register form h2 {
    background: url(../../assets/img/pencil.png) 20px 6px no-repeat;
  }
}

@media (min-width: 768px) and (max-width: 979px) {
  .register form h2 {
    background: none;
  }
}

@media (max-width: 767px) {
  body {
    padding-left: 0;
    padding-right: 0;
  }

  .logo,
  .links {
    text-align: center;
  }

  .links {
    padding-bottom: 5px;
  }

  .logo h1 {
    padding-left: 0;
  }

  .links a.home {
    margin-left: 0;
  }

  .links a.blog {
    margin-right: 0;
  }

  .register-container {
    padding-left: 20px;
    padding-right: 20px;
  }

  .register form h2 {
    background: none;
  }

  .iphone img {
    display: none;
  }
}

@media (max-width: 480px) {
  .register form button {
    width: 97%;
  }
}
</style>

