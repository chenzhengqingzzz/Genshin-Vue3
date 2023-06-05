<template>
  <div id="ysheader">
      <img class="yslogo" src="../assets/yslogo.png" alt="">
      <div class="ys-top-nav">
          <div class="headerindex"></div>
          <!-- <div class="headerindex" :style="msg"></div> -->
          <ul class="ys-nav-ul">
              <!-- <li @click="come" @mouseover="mm1" @mouseleave="leave" class="jj4"><router-link to='/'>首 页</router-link></li>
              <li @click="come" @mouseover="mm2" @mouseleave="leave" class="jj4"><router-link to='/xingwen'>新 闻</router-link></li>
              <li @click="come" @mouseover="mm3" @mouseleave="leave" class="jj4"><router-link to='/jiaose'>角 色</router-link></li>
              <li @click="come" @mouseover="mm4" @mouseleave="leave" class="jj4"><router-link to='/shijie'>世 界</router-link></li>
              <li @click="come" @mouseover="mm5" @mouseleave="leave" class="jj4"><router-link to='/manhua'>漫 画</router-link></li>
              <li @click="come" @mouseover="mm6" @mouseleave="leave" class="jj4"><router-link to='/shequ'>社 区</router-link></li> -->
              <li class="jj1"><router-link to='/'>首 页</router-link></li>
              <li class="jj2"><router-link to='/xingwen'>新 闻</router-link></li>
              <li class="jj3"><router-link to='/jiaose'>角 色</router-link></li>
              <li class="jj4"><router-link to='/shijie'>世 界</router-link></li>
              <li class="jj5"><router-link to='/manhua'>漫 画</router-link></li>
              <li class="jj6"><router-link to='/shequ'>社 区</router-link></li>
          </ul>
      </div>
      <audio class="music1" autoplay="autoplay" loop="true" type="audio/mp3" src="../assets/music/video1.mp3"></audio>
      <audio class="music2" autoplay="autoplay" loop="true" type="audio/mp3" src="../assets/music/video2.mp3"></audio>
  </div>
</template>

<script>
    export default {
        name:"ysheader",
        data() {
            return {
                msg:"left:20px",
                msgg:"left:20px"
            }
        },
        methods: {
            come(){this.msgg = this.msg},
            leave(){this.msg = this.msgg},
            mm1(){this.msg = "left:20px"},
            mm2(){this.msg = "left:121.25px"},
            mm3(){this.msg = "left:222.5px"},
            mm4(){this.msg = "left:323.75px"},
            mm5(){this.msg = "left:425px"},
            mm6(){this.msg = "left:526.25px"},
        }
    }
</script>

<style scope="css">
    #ysheader{
        position: relative;
        left: 0;
        top: 0;
        z-index: 100;
        width: 100%;
        height: 66px;
        transform: translateX(0px);
        opacity: 1;
        box-shadow:0px 3px 7px 0px rgba(0,0,0,0.35);
        background-color:rgba(17,17,17,0.75);
        overflow: hidden;
    }
    .yslogo{
        position: absolute;
        left: 90px;
        top: -40px;
        height: 150px;
        text-align: center;
    }
    .music1,
    .music2{
        position: absolute;
        top: 100px;
    }
    .ys-top-nav{
        position: absolute;
        top: 0;
        left: 280px;
        width: 45%;
        height: 66px;
    }
    .headerindex{
        position: absolute;
        width: 60px;
        height: 5px;
        top: 0;
        background-color: #69e0ff;
        z-index: 10;
        /* (20, 121.25, 222.5, 323.75, 425, 526.25) */
    }
    .ys-nav-ul{
        height: 66px;
        position: absolute;
        font-family:"Microsoft YaHei", "微软雅黑", "MicrosoftJhengHei", "华文细黑", "STHeiti", "MingLiu";
        text-align: center;
    }
    .ys-nav-ul li{
        display: block;
        position: relative;
        float: left;
        margin: 20px 30px !important;
        cursor: pointer;
        font-size: 18px;
        font-size: bold;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        height: 66px;
        width: auto;
        text-align: center;
    }
    .ys-nav-ul li a{
        color: #c7c7c7;
    }
    .ys-nav-ul li a:hover {
        text-shadow: 0 0 10px #69e0ff, 0 0 20px #69e0ff, 0 0 40px #69e0ff;
        color: #fff;
    }
    .jj1:hover~.headerindex{ left:20px; }
    .jj2:hover+.headerindex{ left:121.25px; }
    .jj3:hover+.headerindex{ left:222.5px; }
    .jj4:hover~.headerindex{ left:323.75px; }
    .jj5:hover~.headerindex{ left:425px; }
    .jj6:hover~.headerindex{ left:526.25px; }
</style>