// 这是想要通过第9行a标签做传参路由实现的搁浅版本
<template>
  <div class="background">
    <img src="../../assets/jiaosepage/sanhua.png" alt="" class="sanhua">
    <div class="yxyy">
      <img src="../../assets/jtleft.png" alt="" class="jtleft" @click="dianji(arrow+1)">
      <ul class="jskp">
        <!-- <li v-for="(p) in mdheroxxs.slice(arrow, arrow+6)" :key="p.num" @click="dianji(p.num)"> -->
        <li v-for="(p) in mdheroxxs.slice(arrow, arrow+6)" :key="p.num">
          <a href="https://www.baidu.com/" class="luyou" @click="dianji(p.num)"></a>
          <!-- <img :src="require('../../assets/hero/md0Xq.png')" alt=""> -->
          <img :src="p.xtp" alt="">
          <div class="wz">{{p.name}}</div>
        </li>
      </ul>
      <img src="../../assets/jtrigth.png" alt="" class="jtright" @click="dianji(arrow+3)">
    </div>
  </div>
</template>

<script>

  export default {
    name: 'Mengde',
    data() {
      return {
        arrow : 0,
        mdheroxxs : [
          {num: 0,name: "琴",sex: "女",city: "蒙德",starts: 5,element: "风",arms: "单手剑",
          xtp:require('../../assets/hero/md0Xq.png'),},
          {num: 1,name: "安柏",sex: "女",city: "蒙德",starts: 4,element: "火",arms: "弓",
          xtp:require('../../assets/hero/md1Xab.png'),},
          {num: 2,name: "丽莎",sex: "女",city: "蒙德",starts: 4,element: "雷",arms: "法器",
          xtp:require('../../assets/hero/md2Xls.png'),},
          {num: 3,name: "凯亚",sex: "男",city: "蒙德",starts: 4,element: "冰",arms: "单手剑",
          xtp:require('../../assets/hero/md3Xky.png'),},
          {num: 4,name: "芭芭拉",sex: "女",city: "蒙德",starts: 4,element: "水",arms: "法器",
          xtp:require('../../assets/hero/md4Xbbl.png'),},
          {num: 5,name: "迪卢克",sex: "男",city: "蒙德",starts: 5,element: "火",arms: "双手剑",
          xtp:require('../../assets/hero/md5Xdlk.png'),},
          {num: 6,name: "雷泽",sex: "男",city: "蒙德",starts: 4,element: "雷",arms: "双手剑",
          xtp:require('../../assets/hero/md6Xlz.png'),},
          {num: 7,name: "温迪",sex: "男",city: "蒙德",starts: 5,element: "风",arms: "弓",
          xtp:require('../../assets/hero/md7Xwd.png'),},
          {num: 8,name: "可莉",sex: "女",city: "蒙德",starts: 5,element: "火",arms: "法器",
          xtp:require('../../assets/hero/md8Xkl.png'),},
          {num: 9,name: "班尼特",sex: "男",city: "蒙德",starts: 4,element: "火",arms: "单手剑",
          xtp:require('../../assets/hero/md9Xbnt.png'),},
          {num: 10,name: "诺艾尔",sex: "女",city: "蒙德",starts: 4,element: "岩",arms: "双手剑",
          xtp:require('../../assets/hero/md10Xnae.png'),},
          {num: 11,name: "菲谢尔",sex: "女",city: "蒙德",starts: 4,element: "雷",arms: "弓",
          xtp:require('../../assets/hero/md11Xfxe.png'),},
          {num: 12,name: "砂糖",sex: "女",city: "蒙德",starts: 4,element: "风",arms: "法器",
          xtp:require('../../assets/hero/md12Xst.png'),},
          {num: 13,name: "莫娜",sex: "女",city: "蒙德",starts: 5,element: "水",arms: "法器",
          xtp:require('../../assets/hero/md13Xmn.png'),},
          {num: 14,name: "迪奥娜",sex: "女",city: "蒙德",starts: 4,element: "冰",arms: "弓",
          xtp:require('../../assets/hero/md14Xdan.png'),},
          {num: 15,name: "阿贝多",sex: "男",city: "蒙德",starts: 5,element: "岩",arms: "单手剑",
          xtp:require('../../assets/hero/md15Xabd.png'),},
          {num: 16,name: "罗莎莉亚",sex: "女",city: "蒙德",starts: 4,element: "冰",arms: "枪",
          xtp:require('../../assets/hero/md16Xlsly.png'),},
          {num: 17,name: "优菈",sex: "女",city: "蒙德",starts: 5,element: "冰",arms: "双手剑",
          xtp:require('../../assets/hero/md17Xyl.png'),},
          {num: 18,name: "埃洛伊",sex: "女",city: "蒙德",starts: 5,element: "冰",arms: "弓",
          xtp:require('../../assets/hero/md18Xaly.png'),},
        ],
      }
    },
    methods:{
      dianji(e){
        console.log("点击了",e);
        if(e<3) this.arrow = 0;
        else if(e+4>this.mdheroxxs.length) this.arrow = this.mdheroxxs.length-6;
        else this.arrow = e-2;
      }
    }
  }
</script>

<style scope>
  .background {
    position: relative;
    display: block;
    width: 100%;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    /* background-color: brown; */
    z-index: -1;
    overflow: hidden;
  }
  .sanhua{
    position: absolute;
    width: 76%;
    left: 50%;
    bottom: 0;
    z-index: 1;
    transform: translate(-50%,-2%);
  }
  .yxyy{
    position: absolute;
    width: 100%;
    height: 190px;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 2;
    background-image: linear-gradient(rgba(255,255,255,0.1), rgba(255,255,255,0.2),rgba(0,0,0,0.5));
  }
  .jtleft,
  .jtright{
    position: absolute;
    width: 45px !important;
    height: 64px;
    bottom: 65px;
    left: 50%;
    transform: translate(-1100%);
    z-index: 10 !important;
    cursor:pointer;
  }
  .jtright{
    right: 50%;
    transform: translate(1000%);
  }
  .jskp{
    position: absolute;
    width: 826px;
    height: 130px;
    left: 50%;
    bottom: 30px;
    transform: translate(-50%);
    /* background-color: blanchedalmond; */
  }
  .jskp li{
    position: relative;
    float: left;
    width: 106px;
    height: 128px;
    margin-right: 38px;
    background-image: linear-gradient(to bottom right, rgba(0,0,0,0.6),rgba(0,0,0,0.3), rgba(255,255,255,0.5));
    border-radius: 5px;
    cursor:pointer;
    /* border: 2px solid transparent; */
    /* overflow: hidden; *//* 这个会导致文字有黑边 */
  }
  .jskp li:last-of-type{
    margin-right: 0;
  }
  .jskp li:hover{
    border: 2px solid #fff;
    background-image: linear-gradient(to bottom right, rgba(0,0,0,0.7),rgba(0,0,0,0.5), rgba(255,255,255,0.1));
  }
  .jskp li img{
    position: relative;
    float: left;
    width: 106px;
    height: 106px;
    z-index: 2;
  }
  .luyou{
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: transparent;
    z-index: 4;
  }
  .wz{
    position: relative;
    float: left;
    width: 106px;
    height: 22px;
    left: 50%;
    transform: translate(-50%);
    background-color: black;
    text-align: center;
    color: #fff;
    font-size: 16px;
    border-radius: 0 0 5px 5px;
  }
  .jskp li:hover .wz{
    color: #000 !important;
    background-color: #fff !important;
  }
</style>