<template>
  <div class="index">
    <div class="index-header">
      <div class="nav-menu">
        <div class="nav-menu-box">
          <div class="nav-con fl">
            <ul>
              <li><a href="">主页</a></li>
              <li><a href="">画友</a></li>
              <li><a href="">游戏中心</a></li>
              <li><a href="">直播</a></li>
              <li><a href="">会员</a></li>
            </ul>
          </div>
          <div class="nav-con fr">
            <ul>
              <li><a href="">登录</a></li>
              <li><a href="">注册</a></li>
              <li class="loginImg"><a href=""></a></li>
            </ul>
          </div>
        </div>
      </div>
      <div class="index-search">
        <div class="search-box">
          <input type="text"  class="search-key" placeholder="搜索"/>
          <button type="button" class="search-submit"></button>
        </div>
      </div>
      <div class="banner-link"></div>
      <div class="index-wrapper">
        <div class="primary-menu">
          <ul class="menu-list">
            <li class="home"><a href=""><div class="nav-name">首页</div></a></li>
            <li><a href=""><div class="num-wrap"><span>992</span></div><div class="nav-name">动画</div></a></li>
            <li><a href=""><div class="num-wrap"><span>939</span></div><div class="nav-name">番剧</div></a></li>
            <li><a href=""><div class="num-wrap"><span>991</span></div><div class="nav-name">音乐</div></a></li>
            <li><a href=""><div class="num-wrap"><span>199</span></div><div class="nav-name">舞蹈</div></a></li>
            <li><a href=""><div class="num-wrap"><span>939</span></div><div class="nav-name">游戏</div></a></li>
            <li><a href=""><div class="num-wrap"><span>199</span></div><div class="nav-name">科技</div></a></li>
            <li><a href=""><div class="num-wrap"><span>299</span></div><div class="nav-name">生活</div></a></li>
            <li><a href=""><div class="num-wrap"><span>499</span></div><div class="nav-name">时尚</div></a></li>
            <li><a href=""><div class="num-wrap"><span>599</span></div><div class="nav-name">广告</div></a></li>
            <li><a href=""><div class="num-wrap"><span>499</span></div><div class="nav-name">直播</div></a></li>
            <li><a href=""><div class="num-wrap"><span>499</span></div><div class="nav-name">影视</div></a></li>
            <li><a href=""><div class="num-wrap"><span>569</span></div><div class="nav-name">专栏</div></a></li>
            <li><a href=""><div class="num-wrap"><span>359</span></div><div class="nav-name">平台</div></a></li>
            <li><a href=""><div class="num-wrap"><span>509</span></div><div class="nav-name">活动</div></a></li>
            <li><a href=""><div class="num-wrap"><span>566</span></div><div class="nav-name">赛事</div></a></li>
            <li><a href=""><div class="num-wrap"><span>465</span></div><div class="nav-name">鬼畜</div></a></li>
            <li><a href=""><div class="num-wrap"><span>768</span></div><div class="nav-name">国创</div></a></li>
            <li><a href=""><div class="num-wrap"><span>57</span></div><div class="nav-name">国外</div></a></li>
            <li><a href=""><div class="num-wrap"><span>59</span></div><div class="nav-name">会员</div></a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="index-content">
      <div class="recommend">
        <div class="carousel-box">
          <div class="carousel-content">
            <ul class="pic">
              <li>
                <a href="">
                  <img src="../../static/image/carousel1.jpg"/>
                </a>
              </li>
              <li>
                <a href="">
                  <img src="../../static/image/carousel2.jpg"/>
                </a>
              </li>
              <li>
                <a href="">
                  <img src="../../static/image/carousel3.jpg"/>
                </a>
              </li>
            </ul>
            <ul class="title">
              <li></li>
              <li></li>
              <li></li>
            </ul>
            <ul class="btn">
              <li></li>
              <li></li>
              <li></li>
            </ul>
          </div>
        </div>
        <div class="recommend-content"></div>
      </div>
    </div>
  </div>
</template>

<script>
  import $ from "jquery";
  export default {
    name: 'index',
    data () {
      return {

      }
    },
    mounted(){
      let _this=this;
      let timer = setInterval(function(){
        let a = $('.pic').css("margin-left");
        let w = $('.pic').css("width");
        a=a.replace("px","");
        w=w.replace("px","");
        if(Math.abs(a)>=Math.abs(w/2)){
          $('.pic').css("margin-left","0");
        }else{
          $('.pic').css("margin-left",a-440+"px");
        }
      },5000);

    },
    methods:{
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.index-header{
  width:100%;
  position: relative;
}
/*导航栏*/
.nav-menu{
  z-index:200;
  width:100%;
  position: absolute;
  top:0;
  left:0;
  box-shadow:0 1px 2px rgba(0,0,0,0.1);
  color:black;
  background-color: rgba(255,255,255,0.55);
}
.nav-menu-box{
  width:980px;
  margin:0 auto;
  height:42px;
}
/*@media screen and (min-width:1400px){
  .nav-menu-box{
    width:1160px;
  }
}*/
.nav-menu-box .fl{
  display: inline;
}
.nav-menu-box .fr{
  display: inline;
}
.nav-menu-box .fl>ul>li,.nav-menu-box .fr>ul>li{
  float: left;
  display: block;
  text-align: center;
  height:42px;
  line-height: 42px;
}
.nav-menu-box .fr>ul>li{float:right;}
.loginImg>a{
  height:42px;
  width:22px;
  margin:0 10px;
  border-radius:50%;
  background-size:100%;
  background-position: right center;
  background-image:url(../../static/image/00.jpg);
}
.nav-menu-box .fl>ul>li>a,.nav-menu-box .fr>ul>li>a{
  color:black;
  padding:0 10px;
  height:100%;
  display: block;
  transition:all .2s;
}
.nav-menu-box .fl>ul>li>a,.nav-menu-box .fr>ul>li>a:hover{
  background-color: rgba(255,255,255,.7);
}
/*搜索*/
.index-search{
  width:980px;
  height:170px;
  position: relative;
  z-index:100;
  margin:0 auto;
}
.search-box{
  position:absolute;
  right:0;
  bottom:20px;
  width:268px;
  height:32px;
  padding:2px;
  border-radius:4px;
  display: block;
  background-color:rgba(255,255,255,0.88);
  transition:background-color .2s;
}
.search-box:hover{
  background-color:rgba(255,255,255,1);
}
.search-key{
  float:left;
  width:200px;
  color:#222;
  font-size:12px;
  overflow: hidden;
  height:32px;
  padding:0 12px;
  border:0;
  box-shadow:none;
  background-color:transparent;
}
.search-submit{
  display: block;
  position: absolute;
  right:0;
  width:48px;
  min-width:0;
  cursor:pointer;
  height:32px;
  margin:0;
  padding:0;
  border:0;
  background:url(../../static/image/search.png) center;
  background-size:50%;
  background-repeat: no-repeat;
}
/*banner*/
.banner-link{
  background-image:url(../../static/image/nav2.jpg);
  background-repeat:no-repeat;
  background-position: center center;
  position: absolute;
  top:0;
  height:170px;
  width:100%;
  z-index:99;
}
/*菜单*/
.index-wrapper{
  width:980px;
  margin:0 auto;
}
.primary-menu{
  margin:0 auto;
  width:980px;
  height:50px;
  padding:8px 0 0;
  margin-bottom:4px;
}
.menu-list{
  display: inline-block;
  height:42px;
  color:#222;
}
.menu-list .home>a{
  background:url(../../static/image/home.png) center center no-repeat;
  background-size:50% ;
  height:28px;
}
.menu-list>li{
  float:left;
  display: block;
  position: relative;
}
.menu-list>li>a{
  width:48px;
  text-align: center;
  display: block;
}
.menu-list>li>a .num-wrap{
  position: absolute;
  top:8px;
  left:0;
  height:14px;
  width:100%;
  text-align: center;
}
.menu-list>li>a .num-wrap>span{
  display: inline-block;
  vertical-align: top;
  font-size: 12px;
  color:white;
  background-color:#ffafc9;
  border-radius: 3px;
  height:12px;
  line-height: 14px;
  max-width:28px;
  padding:1px 3px;
}
.menu-list>li>a .nav-name{
  vertical-align: middle;
  color:#222;
  font-size:12px;
  height:40px;
  line-height: 50px;
  padding-top:8px;
}
/*内容部分*/
.index-content{
  width:980px;
  margin:0 auto;
}
.recommend{
  padding-bottom:40px;
}
.carousel-box{
  width:440px;
  height:220px;
  float:left;
}
.carousel-box .carousel-content{
  width:100%;
  height:100%;
  position: relative;
  border-radius: 4px;
  overflow: hidden;
}
.carousel-box .carousel-content .pic{
  width:300%;
  margin-left:0%;
  transition: all .3s;
  -webkit-transition: all .3s;
}
.carousel-box .carousel-content ul li{
  float:left;
}
</style>
