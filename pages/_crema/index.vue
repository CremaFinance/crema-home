<template>
  <div class="outer">
    <!-- 背景图位置 -->
    <img class="bgOne" src="../../assets/img/cremaWebImg/bg-img2@2x.png" alt="">
    <img class="bgTwo" src="../../assets/img/cremaWebImg/bg-img1@2x.png" alt="">
    <img class="bgThree" src="../../assets/img/cremaWebImg/bg-img3@2x.png" alt="">
    <img class="bgFour" src="../../assets/img/cremaWebImg/bg-img4@2x.png" alt="">
    <img class="bgFive" src="../../assets/img/cremaWebImg/bg-img5@2x.png" alt="">
    <img class="bgSix" src="../../assets/img/cremaWebImg/bg-img6@2x.png" alt="">
    <!-- <video muted="muted" loop="true" autoplay="autoplay" controls="controls">
        <source src="../../assets/img/cremaWebImg/Color_Lines_Logo.mp4" type="video/mp4">
    </video> -->
    <!-- 头部导航栏区域 -->
    <div class="header">
      <div class="navLeft">
        <img src="../../assets/img/cremaWebImg/headerLogo.png">
      </div>
      <div class="navReight">
        <a v-if="!isBirdie" @mouseover="isBirdie = !isBirdie" href="https://twitter.com/Crema_Finance" target="_blank"><img src="../../assets/img/cremaWebImg/icon_twitter@2x.png" alt=""></a>
        <a v-else="isBirdie" @mouseleave="isBirdie = !isBirdie" href="https://twitter.com/Crema_Finance" target="_blank"><img src="../../assets/img/cremaWebImg/twitter@2x.png" alt=""></a>
        <a v-if="!isAircraft" @mouseover="isAircraft = !isAircraft" href="https://t.me/cremafinance" target="_blank"><img src="../../assets/img/cremaWebImg/icon_Telegram Group@2x.png" alt=""></a>
        <a v-else="isAircraft" @mouseleave="isAircraft = !isAircraft" href="https://t.me/cremafinance" target="_blank"><img src="../../assets/img/cremaWebImg/telegram@2x.png" alt=""></a>
        <a v-if="!isLetter" @mouseover="isLetter = !isLetter" href="https://medium.com/@hello_9645" target="_blank"><img src="../../assets/img/cremaWebImg/icon_Medium@2x.png" alt=""></a>
        <a v-else="isLetter" @mouseleave="isLetter = !isLetter" href="https://medium.com/@hello_9645" target="_blank"><img src="../../assets/img/cremaWebImg/medium@2x.png" alt=""></a>
        <a v-if="!isRobot" @mouseover="isRobot = !isRobot" href="https://discord.gg/5bVg7frrkr" target="_blank"><img src="../../assets/img/cremaWebImg/icon_Discord@2x.png" alt=""></a>
        <a v-else="isRobot" @mouseleave="isRobot = !isRobot" href="https://discord.gg/5bVg7frrkr" target="_blank"><img src="../../assets/img/cremaWebImg/discord@2x.png" alt=""></a>
      </div>
    </div>
    <!-- 主体区域 -->
    <div class="main">
      <div class="top">
        <div class="topHeader">
          <div class="topTitle">
            <img src="../../assets/img/cremaWebImg/headerTitle.png" alt="">
          </div>
          <div class="topmain">A Powerful Concentrated Liquidity Protocol.</div>
          <a v-if="!isTopBtn" @mouseover="isTopBtn = !isTopBtn" href="https://app.crema.finance/" target="_blank" class="topBtn">LAUNCH APP</a>
          <a v-else="isTopBtn" @mouseleave="isTopBtn = !isTopBtn" href="https://app.crema.finance/" target="_blank" class="topBtnA">LAUNCH APP</a>
          <div class="gradient"></div>
        </div>
        <div class="topImg">
          <img class="topImg-one" src="../../assets/img/cremaWebImg/headerExamples.png" alt="">
          <img class="topImg-two" src="../../assets/img/cremaWebImg/img-banner-halo@2x.png" alt="">
          <img class="topImg-three" src="../../assets/img/cremaWebImg/img-banner-C@2x.png" alt="">
          <img class="topImg-four" src="../../assets/img/cremaWebImg/img-banner-A@2x.png" alt="">
          <img class="topImg-five" src="../../assets/img/cremaWebImg/img-banner-R@2x.png" alt="">
          <img class="topImg-six" src="../../assets/img/cremaWebImg/img-banner-M@2x.png" alt="">
          <img class="topImg-seven" src="../../assets/img/cremaWebImg/img-banner-E@2x.png" alt="">
        </div>
      </div>
      <div class="center">
        <div class="centerTop centerAll">
          <div class="centerTopLeft">
            <div class="Conce">Concentrated Liquidity Market Maker</div>
            <div class="CLMM">The CLMM algorithm designed by Crema allows users to set their desired orice ranges flexibly when adding liquidity.</div>
          </div>
          <div class="centerTopReight">
            <img src="../../assets/img/cremaWebImg/img-1@2x.png" alt="">
            <img class="floatOne" src="../../assets/img/cremaWebImg/img-triangle1@2x.png" alt="">
            <img class="floatTwo" src="../../assets/img/cremaWebImg/img-circular2@2x.png" alt="">
            <img class="floatThree" src="../../assets/img/cremaWebImg/img-circular1@2x.png" alt="">
          </div>
        </div>
        <div class="centerMain centerAll">
          <div class="centerTopLeft">
            <div class="Conce">Say Goodbye To Impermanent Loss</div>
            <div class="CLMM">Protected by CLMM price bands, liquidity providers can enjoy the best capital efficiency with impermanent loss eliminated.</div>
          </div>
          <div class="centerTopReight">
            <img src="../../assets/img/cremaWebImg/img-2@2x.png" alt="">
            <img class="floatOne" src="../../assets/img/cremaWebImg/img-polygon1@2x.png" alt="">
            <img class="floatTwo" src="../../assets/img/cremaWebImg/img-circular3@2x.png" alt="">
            <img class="floatThree" src="../../assets/img/cremaWebImg/img-cube@2x.png" alt="">
          </div>
        </div>
        <div class="centerBottom centerAll">
          <div class="centerTopLeft">
            <div class="Conce">Ready-To-Integrate DeFi Module</div>
            <div class="CLMM">The concentrated liquidity protocol of Crema can be easily integrated to any DAPPs in Solana ecosystem to aggregate the market depth.</div>
          </div>
          <div class="centerTopReight">
            <img src="../../assets/img/cremaWebImg/img-3@2x.png" alt="">
            <img class="floatOne" src="../../assets/img/cremaWebImg/icon-more@2x.png" alt="">
            <img class="floatTwo" src="../../assets/img/cremaWebImg/icon-mercurial@2x.png" alt="">
            <img class="floatThree" src="../../assets/img/cremaWebImg/icon-crema@2x.png" alt="">
            <img class="floatFour" src="../../assets/img/cremaWebImg/icon-sol@2x.png" alt="">
          </div>
        </div>
      </div>
      <div class="bottom">
        <div class="botTop">Roadmap</div>
        <div class="botCenter">
          <div class="botCenterAll">
              <div class="botCenterOct bCter">2021 Nov</div>
              <div class="botCenterNov bCter">2021 Dec</div>
              <div class="botCenterDec bCter">2022 Jan</div>
              <div class="botCenterQ bCter">2022 Feb-March</div>
          </div>
        </div>
        <div class="botBottom">
          <div class="botBottomPro botBottomAll">
            <p>Project Started</p>
            <p>R&D Started</p>
            <p>Seed Round Funding</p>
          </div>
          <div class="botBottomFun botBottomAll">
            <p>MVP Release</p>
            <p>Integrate CLMM Pool to Aggregators</p>
          </div>
          <div class="botBottomFar botBottomAll">
            <p>TGE & IDO</p>
            <p>Official V1 Release</p>
            <p>LP NFT Farming Started</p>
          </div>
          <div class="botBottomCLMM botBottomAll">
            <p>CLMM V2</p>
            <p>vCRM function</p>
            <p>DAO Platform</p>
            <p>Liduidity Migration</p>
          </div>
        </div>
      </div>
    </div>
    <!-- 底部区域 -->
    <div class="footer">
      <div class="footerAll">
        <div class="footerLeft">
          <img src="../../assets/img/cremaWebImg/footerLogo.png" alt="">
          <p>© 2021 Crema. All rights reserved.</p>
        </div>
        <div class="footerReight">
          <div class="ReiImg">
            <a href="https://twitter.com/Crema_Finance" target="_blank"><img src="../../assets/img/cremaWebImg/icon_twitter@2x.png" alt=""></a>
            <a href="https://t.me/cremafinance" target="_blank"><img src="../../assets/img/cremaWebImg/icon_Telegram Group@2x.png" alt=""></a>
            <a href="https://medium.com/@hello_9645" target="_blank"><img src="../../assets/img/cremaWebImg/icon_Medium@2x.png" alt=""></a>
            <a href="https://discord.gg/5bVg7frrkr" target="_blank"><img src="../../assets/img/cremaWebImg/icon_Discord@2x.png" alt=""></a>
          </div>
          <p>hello@crema.finance</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { setCookie, getCookie } from "~/assets/js/cookie";
export default {
  data() {
    return {
      iosItem: "",
      androidItem: "",
      isShow: false,
      isShow1: false,
      isShow2: false,
      isShow3: false,
      isShow4: false,
      showActive: 1,
      isTopBtn:false,
      isBirdie:false,
      isAircraft:false,
      isLetter:false,
      isRobot:false,
      localeList: [
        {
          label: "English",
          key: "en",
        },
        {
          label: "简体中文",
          key: "zh",
        },
      ],
      localObj: {
        en: {
          key: "English",
        },
        zh: {
          key: "简体中文",
        },
      },
      // locale: "简体中文",
    };
  },
  computed: {
    locale() {
      return this.$store.state.locale;
    },
    version() {
      if (this.androidItem) {
        if (this.isAndroidOrIOS() === 3) {
          return this.androidItem.version;
        }
      }
      if (this.iosItem) {
        if (this.isAndroidOrIOS() === 2) {
          return this.iosItem.version;
        }
      }
      return "xx.xx.xx";
    },
  },
  mounted() {},
  methods: {
    mouseOver() {
      this.openList();
    },
    mouseLeave() {
      this.hideList();
    },
    openList() {
      this.isShow = true;
    },
    hideList() {
      this.isShow = false;
    },
    toggle() {
      this.isShow = !this.isShow;
    },
    switchLanguage(lang, index) {
      this.showActive = index;
      setCookie("lang", lang);
      // console.log('this.$route####', this.$route);
      this.$store.dispatch("setLanguage", lang);
      this.$i18n.locale = lang;
    },
    goUrl(type) {
      if (type == "android") {
        window.location.href = this.androidItem.url;

        // "https://archive.kkwallet.org/upload/package/1617767590768594342.apk";
      }
    },
    isAndroidOrIOS() {
      if (process.client) {
        const h5_type = {
          web: 1,
          ios: 2,
          android: 3,
        };
        let _type = h5_type.web;
        var u = window.navigator.userAgent;
        if (u.indexOf("Android") > -1 || u.indexOf("Adr") > -1) {
          // android终端
          _type = h5_type.android;
        }
        if (!!u.match(/\(i[^;]+;( U;)? CPU.+Mac OS X/)) {
          // ios终端
          _type = h5_type.ios;
        }
        return _type;
      }
    },
  },
};
</script>
<style lang="scss" scoped>

@keyframes icon {
  0% {
      // opacity: 0.8;
      transform: translate(0, 0);
  }
  50% {
      transform: translate(0px, 15px);
  }
  100% {
      transform: translate(0, 0);
  }
}
@keyframes iconK {
  0% {
      transform: translate(0, 0);
  }
  50% {
      transform: translate(0px, 23px);
  }
  100% {
      transform: translate(0, 0);
  }
}
@keyframes iconM {
  0% {
      transform: translate(0, 0);
  }
  50% {
      transform: translate(0px, 30px);
  }
  100% {
      transform: translate(0, 0);
  }
}
@-webkit-keyframes rotation {
  from {
      -webkit-transform: rotate(0deg);
  }
  to {
      -webkit-transform: rotate(360deg);
  }
}
.outer {
  width: 100%;
  height: 100%;
  background: #14191E;
  position: relative;
  .bgOne{
    position: absolute;
    width: 335px;
    height: 387px;
    left: 0;
    top: 528px;
  }
  .bgTwo{
    position: absolute;
    width: 453px;
    height: 769px;
    top: 95px;
    right: 0;
  }
  .bgThree{
    position: absolute;
    width: 210px;
    height: 398px;
    top: 1641px;
    right: 0;
  }
  .bgFour{
    position: absolute;
    width: 451px;
    height: 769px;
    left: 0;
    top: 1281px;
  }
  .bgFive{
    position: absolute;
    width: 719px;
    height: 1428px;
    right: 0;
    top: 566px;
  }
  .bgSix{
    position: absolute;
    width: 610px;
    height: 929px;
    right: 0;
    top: 1140px;
  }
  // video{
  //   position: absolute;
  //   width: 100%;
  //   height: 500px;
  //   top: 163px;
  // }
  .header {
    width: 1100px;
    height: 163px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 auto;
    .navLeft{
      width: 180px;
      height: 43px;
      img{
        width: 180px;
        height: 43px;
      }
    }
    .navReight{
      width: 170px;
      height: 20px;
      display: flex;
      justify-content: space-between;
      img{
        width: 20px;
        height: 20px;
      }
    }
  }
  .main{
    width: 100%;
    height: 2019px;
    padding: 10px 0 0 0;
    // background: #bfa;
    .top{
      height: 386px;
      width: 1100px;
      // background: #bbb;
      display: flex;
      justify-content: space-between;
      margin: 0 auto;
      .topHeader{
        width: 493px;
        height: 386px;
        // background:#bfa;
        position: relative;
        .topTitle{
          width: 484px;
          height: 51px;
          margin-top: 108px;
          position: relative;
          z-index: 20;
          img{
            width: 484px;
            height: 51px;
          }
        }
        .topmain{
          width: 505px;
          height: 40px;
          font-size: 24px;
          font-family: 'Avenir';
          color: #fff;
          margin-top: 29px;
        }
        .topBtn{
          display: block;
          width: 163px;
          height: 54px;
          border-radius: 27px;
          background: linear-gradient(221deg, #4CFFDF 0%, #4E90FA 100%);
          text-align: center;
          line-height: 54px;
          color: #fff;
          font-size: 16px;
          font-weight: 900;
          font-family: 'Arial-Black';
          margin-top: 28px;
        }
        .topBtnA{
          display: block;
          width: 163px;
          height: 54px;
          border-radius: 27px;
          background: linear-gradient(223deg, #A6FFEF 0%, #7AAEFF 100%);
          text-align: center;
          line-height: 54px;
          color: #fff;
          font-size: 16px;
          font-weight: 900;
          font-family: 'Arial-Black';
          margin-top: 28px;
        }
        .gradient{
          position: absolute;
          left: 0;
          top: 148px;
          width: 177px;
          height: 20px;
          background: linear-gradient(39deg, rgba(43,255,168,0.5) 0%, rgba(0,100,255,0.5) 100%);
          z-index: 2;
        }
      }
      .topImg{
        width: 514px;
        height: 386px;
        position: relative;
        .topImg-one{
          position: absolute;
          top: 24px;
          left: 12px;
          width: 446px;
          height: 328px;
        }
        .topImg-two{
          width: 300px;
          height: 300px;
          position: absolute;
          top: 16px;
          left: 74px;
          -webkit-transform: rotate(360deg);
          -webkit-animation: rotation 3s linear infinite;
        }
        .topImg-three{
          position: absolute;
          width: 56px;
          height: 84px;
          top: 34px;
          left: 10px;
          animation: icon 3s linear infinite;
        }
        .topImg-four{
          position: absolute;
          width: 73px;
          height: 73px;
          top: 38px;
          left: 315px;
          animation: icon 5s linear infinite;
        }
        .topImg-five{
          position: absolute;
          width: 63px;
          height: 73px;
          top: 180px;
          left: 46px;
          animation: iconM 4s linear infinite;
        }
        .topImg-six{
          position: absolute;
          width: 92px;
          height: 73px;
          top: 152px;
          left: 417px;
          animation: iconK 3s linear infinite;
        }
        .topImg-seven{
          position: absolute;
          width: 47px;
          height: 73px;
          top: 300px;
          left: 258px;
          animation: icon 8s linear infinite;
        }
      }
    }
    .center{
      height: 984px;
      width: 100%;
      // background: #ccc;
      margin-top: 145px;
      .centerAll{
        width: 1100px;
        height: 288px;
        background: rgba(255, 255, 255, 0.05);
        border-radius: 30px;
        padding: 0 0 0 40px;
        display: flex;
        margin: 0 auto;
        justify-content: space-between;
        .centerTopLeft{
          width: 572px;
          height: 288px;
          padding: 50px 0 50px;
          display: flex;
          flex-wrap: wrap;
          align-content: space-around;
          .Conce{
            width: 572px;
            font-size: 28px;
            font-family: 'Montserrat-Bold';
            color: #fff;
          }
          .CLMM{
            width: 446px;
            color: #959CAC;
            font-size: 20px;
            height: 108px;
            line-height: 36px;
            font-family: 'Avenir';
          }
        }
        .centerTopReight{
          width: 420px;
          height: 288px;
          img{
            width: 420px;
            height: 288px;
          }
          // .floatOne{
          //   animation: icon 3s linear infinite;
          // }
          // .floatTwo{
          //   animation: icon 3s linear infinite;
          // }
          // .floatThree{
          //   animation: icon 3s linear infinite;
          // }
          // .floatFour{
          //   animation: icon 3s linear infinite;
          // }
        }
      }
      .centerTop{
        .centerTopReight{
          position: relative;
          .floatOne{
            position: absolute;
            left: 83px;
            top: 32px;
            width: 21px;
            height: 21px;
            animation: iconM 5s linear infinite;
          }
          .floatTwo{
            position: absolute;
            left: 333px;
            top: 96px;
            width: 19px;
            height: 18px;
            animation: icon 3s linear infinite;
          }
          .floatThree{
            position: absolute;
            left: 87px;
            top: 212px;
            width: 28px;
            height: 28px;
            animation: iconK 4s linear infinite;
          }
        }
      }
      .centerMain{
        margin-top: 60px;
        .centerTopReight{
          position: relative;
          .floatOne{
            position: absolute;
            left: 114px;
            top: 29px;
            width: 19px;
            height: 19px;
            animation: iconM 2s linear infinite;
          }
          .floatTwo{
            position: absolute;
            left: 269px;
            top: 156px;
            width: 47px;
            height: 46px;
            animation: iconK 4s linear infinite;
          }
          .floatThree{
            position: absolute;
            left: 89px;
            top: 135px;
            width: 95px;
            height: 96px;
            animation: icon 3s linear infinite;
          }
        }
      }
      .centerBottom{
        margin-top: 60px;
        .centerTopReight{
          position: relative;
          .floatOne{
            position: absolute;
            left: 173px;
            top: 44px;
            width: 77px;
            height: 77px;
            animation: icon 4s linear infinite;
          }
          .floatTwo{
            position: absolute;
            left: 94px;
            top: 74px;
            width: 78px;
            height: 78px;
            animation: iconM 4s linear infinite;
          }
          .floatThree{
            position: absolute;
            left: 249px;
            top: 74px;
            width: 79px;
            height: 78px;
            animation: iconK 4s linear infinite;
          }
          .floatFour{
            position: absolute;
            left: 156px;
            top: 90px;
            width: 111px;
            height: 111px;
            animation: iconM 4s linear infinite;
          }
        }
      }
    }
    .bottom{
      height: 364px;
      width: 100%;
      // background: #ddd;
      margin-top: 120px;
      position: relative;
      z-index: 200;
      .botTop{
        width: 1100px;
        height: 20px;
        margin: 0 auto;
        color: #fff;
        font-size: 24px;
        font-family: 'SansSerifExbFLF';
      }
      .botCenter{
        width: 100%;
        height: 60px;
        background: rgba(255, 255, 255, 0.05);
        margin-top: 53px;
        .botCenterAll{
          width: 1100px;
          height: 60px;
          // background: #000;
          margin: 0 auto;
          display: flex;
          justify-content: space-between;
          .bCter{
            width: 200px;
            height: 60px;
            background: linear-gradient(224deg, rgba(172,255,240,0.2) 0%, rgba(144,156,255,0.2) 45%, rgba(237,176,255,0.2) 100%);
            border-radius: 10px;
            text-align: center;
            line-height: 60px;
            color: #fff;
            font-size: 20px;
            font-family: 'SansSerifExbFLF';
          }
        }
      }
      .botBottom{
        width: 1100px;
        height: 90px;
        margin: 32px auto 0;
        display: flex;
        justify-content: space-between;
        .botBottomAll{
          width: 230px;
          height: 90px;
          color: #959CAC;
          display: flex;
          flex-wrap: wrap;
          p{
            width: 100%;
            font-family: 'Avenir';
            font-size: 18px;
            line-height: 40px;
          }
        }
        .botBottomPro{
          width: 255px;
        }
        .botBottomFun{
          width: 250px;
        }
        .botBottomFar{
          width: 246px;
        }
        .botBottomCLMM{
          width: 195px;
        }
      }
    }
  }
  .footer{
    height: 180px;
    width: 100%;
    background: #232323;
    padding: 40px 0 40px 0;
    .footerAll{
      width: 1100px;
      height: 100px;
      margin: 0 auto;
      // background: #000;
      display: flex;
      justify-content: space-between;
      .footerLeft{
        width: 280px;
        height: 100px;
        display: flex;
        flex-wrap: wrap;
        align-content: space-around;
        img{
          width: 110px;
          height: 26px;
        }
        p{
          font-size: 16px;
          color: rgba(255,255,255,0.5);
          font-family: 'Avenir';
        }
      }
      .footerReight{
        width: 170px;
        height: 100px;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: flex-end;
        .ReiImg{
          display: flex;
          justify-content: space-between;
          width: 170px;
          height: 20px;
          text-align: right;
          img{
            width: 20px;
            height: 20px;
          }
        }
        p{
          font-size: 16px;
          color: rgba(255,255,255,0.5);
          text-align: right;
          font-family: 'Avenir';
        }
      }
    }
  }
}
@keyframes bounce-down {
  25% {
    transform: translateY(-4px);
  }
  50%,
  100% {
    transform: translateY(0);
  }
  75% {
    transform: translateY(4px);
  }
}
@keyframes bounce-opcity {
  25% {
    // opacity: 0.5;
  }
  // 40%{
  //      opacity: 0.3;
  // }
  50% {
    // opacity: 0;
  }
  75% {
    // opacity: 0.5;
  }
  // 75% {
  //      opacity: 0.9;
  // }
  100% {
    // opacity: 1;
  }
}
@media screen and (max-width: 750px) {
  .outer {
    // background: #bae;
    .bgOne{
      display: none;
    }
    .bgTwo{
      display: none;
    }
    .bgThree{
      display: none;
    }
    .bgFour{
      display: none;
    }
    .bgFive{
      display: none;
    }
    .bgSix{
      display: none;
    }
    .header{
      // padding: 0 20px 0;
      // display: none;
      width: 345px;
      height: 101px;
      .navLeft{
        width: 91px;
        height: 21px;
        img{
          width: 91px;
          height: 21px;
        }
      }
      .navReight{
        width: 112px;
        height: 16px;
        img{
          width: 16px;
          height: 16px;
        }
      }
    }
    .main{
      // display: none;
      padding: 0 20px 0;
      height: 2441px;
      .top{
        width: 335px;
        height: 478px;
        flex-wrap: wrap;
        .topHeader{
          height: 136px;
          width: 335px;
          .topTitle{
            width: 329px;
            height: 34px;
            margin-top: 0;
            img{
              width: 329px;
              height: 34px;
            }
          }
          .topmain{
            width: 328px;
            height: 16px;
            font-size: 16px;
            margin-top: 26px;
          }
          .topBtn{
            width: 111px;
            height: 36px;
            font-size: 12px;
            border-radius: 18px;
            line-height: 36px;
            margin: 24px auto 0;
          }
          .topBtnA{
            width: 111px;
            height: 36px;
            font-size: 12px;
            border-radius: 18px;
            line-height: 36px;
            margin: 24px auto 0;
          }
          .gradient{
            width: 120px;
            height: 13px;
            top: 27px;
          }
        }
        .topImg{
          // display: none;
          width: 335px;
          height: 252px;
          .topImg-one{
            width: 290px;
            height: 216px;
            left: 28px;
            top: 18px;
          }
          .topImg-two{
            width: 228px;
            height: 227px;
            left: 54px;
            top: 0;
          }
          .topImg-three{
            width: 37px;
            height: 56px;
            left: 18px;
            top: 20px;
          }
          .topImg-four{
            width: 48px;
            height: 48px;
            left: 232px;
            top: 24px;
          }
          .topImg-five{
            width: 42px;
            height: 48px;
            left: 22px;
            top: 123px;
          }
          .topImg-six{
            width: 61px;
            height: 48px;
            left: 274px;
            top: 107px;
          }
          .topImg-seven{
            width: 31px;
            height: 48px;
            left: 181px;
            top: 204px;
          }
        }
      }
      .center{
        // display: none;
        height: 1325px;
        width: 100%;
        margin-top: 0;
        .centerAll{
          width: 335px;
          height: 402px;
          border-radius: 24px;
          padding: 20px 0 0 0;
          flex-wrap: wrap;
          .centerTopLeft{
            width: 305px;
            padding:0 0 0 10px;
            height: 132px;
            .Conce{
              width: 305px;
              height: 16px;
              font-size: 15px;
            }
            .CLMM{
              width: 295px;
              height: 96px;
              font-size: 16px;
              line-height: 24px;
            }
          }
          .centerTopReight{
            width: 335px;
            height: 230px;
            margin-top: 20px;
            img{
              width: 335px;
              height: 230px;
            }
          }
        }
        .centerTop{
          .centerTopReight{
            .floatOne{
              left: 39px;
              top: 6px;
            }
            .floatTwo{
              left: 288px;
              top: 69px;
            }
            .floatThree{
              left: 42px;
              top: 166px;
            }
          }
        }
        .centerMain{
          .centerTopReight{
            .floatOne{
              left: 78px;
              top: 29px;
            }
            .floatTwo{
              left: 218px;
              top: 135px;
            }
            .floatThree{
              left: 55px;
              top: 106px;
            }
          }
        }
        .centerBottom{
          .centerTopReight{
            .floatOne{
              left : 130px;
              top : 12px;
            }
            .floatTwo{
              left: 66px;
              top: 46px;
            }
            .floatThree{
              left: 191px;
              top: 46px;
            }
            .floatFour{
              left: 114px;
              top: 50px;
            }
          }
        }
      }
      .bottom{
        // display: none;
        height: 595px;
        margin-top: 32px;
        .botTop{
          width: 335px;
        }
        .botCenter{
          background: rgba(255,255,255,0);
          margin-top: 32px;
          .botCenterAll{
            width: 128px;
            height: 540px;
            flex-wrap: wrap;
            margin: 0 0 0 10px;
            .bCter{
              width: 128px;
              height: 36px;
              line-height: 36px;
              font-size: 14px;
            }
          }
        }
        .botBottom{
          // display: none;
          width: 245px;
          height: 540px;
          flex-wrap: wrap;
          margin: -17px 0 0 110px;
          .botBottomAll{
            p{
              line-height: 25px;
            }
          }
        }
      }
    }
    .footer{
      // display: none;
      width: 100%;
      height: 200px;
      padding: 0 0 0 0;
      .footerAll{
        width: 375px;
        height: 200px;
        flex-wrap: wrap;
        position: relative;
        .footerLeft{
          margin: 0 auto;
          height: 200px;
          img{
            margin: 0 auto;
          }
          p{
            margin: 0 auto;
          }
        }
        .footerReight{
          // display: none;
          position: absolute;
          height: 66px;
          left: 106px;
          top: 71px;
          margin: 0 auto;
          p{
            margin: 0 auto;
          }
        }
      }
    }
  }
}
</style>