<template>
  <div class="outer">
    <!-- 背景图 -->
    <!-- <div class="backGroundOne">
      <img src="../../assets/img/cremaImg/bg1@2x.png" alt="">
    </div> -->
    <!-- <div class="backGroundTwo">
      <img src="../../assets/img/cremaImg/tuoyuanxingbeifen7@2x.png" alt="">
    </div> -->
    <!-- <div class="backGroundThree">
      <img src="../../assets/img/cremaImg/tuoyuanxingbeifen7@2x.png" alt="">
    </div> -->
    <!-- <div class="backGroundFour">
      <img src="../../assets/img/cremaImg/bg2@2x.png" alt="">
    </div> -->
    <!-- <div class="backGroundFive">
      <img src="../../assets/img/cremaImg/cameloid9@2x.png" alt="">
    </div> -->

    <!-- 页面部分 -->
    <div class="core">
      <!-- 头部区域 -->
      <div class="header">
        <div class="top">
          <div class="left">
            <img src="../../assets/img/cremaImg/logo@2x.png" alt="">
          </div>
          <div class="reight">
            <a class="herderreightImg" href="https://twitter.com/Crema18403445" target="_blank"><img src="../../assets/img/cremaImg/twitter@2x.png" alt=""></a>
            <a class="herderreightImg" href="https://t.me/cremafinance" target="_blank"><img src="../../assets/img/cremaImg/telegram@2x.png" alt=""></a>
            <a class="herderreightImg" href="https://medium.com/@hello_9645" target="_blank"><img src="../../assets/img/cremaImg/medium@2x.png" alt=""></a>
            <a href="https://discord.gg/5bVg7frrkr" target="_blank"><img src="../../assets/img/cremaImg/discord@2x.png" alt=""></a>
          </div>
        </div>
      </div>
      <!-- 主体部分 -->
      <div class="main">
        <div class="mainAll">
          <div class="backGroundOne">
            <img src="../../assets/img/cremaImg/bg1@2x.png" alt="">
          </div>
          <div class="mainLeft">
            <div class="mainTop">
              <span>Crema Finance</span>
            </div>
            <div class="mainCenter">
              <span>A Powerful Concentrated Liquidity Protocol.</span>
            </div>
            <div class="mainBottom">
              <button class="BtnLeft" v-if="!isShow1" @mouseover="isShow1=!isShow1">LAUNCH APP</button>
              <button class="BtnLeft" v-else @mouseleave="isShow1=!isShow1">Coming Soon</button>
              <button class="BtnReight">DECK</button>
            </div>
          </div>
          <video muted="muted" loop="true" autoplay="autoplay" controls="controls">
              <source src="../../assets/img/cremaImg/fourVideo.mp4" type="video/mp4">
          </video>
          <!-- gif动图展示 -->
          <!-- <div class="mainReight">
              <img src="../../assets/img/cremaImg/leaves.gif" alt="">
          </div> -->
        </div>
      </div>
      <!-- 插图区域 -->
      <div class="plugIn">
          <div class="plugInAll">
            <div class="backGroundTwo">
              <img src="../../assets/img/cremaImg/tuoyuanxingbeifen7@2x.png" alt="">
            </div>
            <div class="backGroundThree">
              <img src="../../assets/img/cremaImg/tuoyuanxingbeifen7@2x.png" alt="">
            </div>
            <div class="OneplugIn">
                <div class="Oneleft">
                    <div class="OneTop">Concentrated Liquidity Market Maker</div>
                    <div class="OneBottom">The CLMM algorithm designed by Crema allows users to set their desired price ranges flexibly when adding liquidity.</div>
                </div>
                <div class="OneReight">
                  <img src="../../assets/img/cremaImg/icon1@2x.png" alt="">
                </div>
            </div>
            <div class="TwoplugIn">
                <div class="Oneleft">
                    <div class="OneTop">Say Goodbye To Impermanent Loss</div>
                    <div class="OneBottom">Protected by CLMM price bands, liquidity providers can enjoy the best capital efficiency with impermanent loss eliminated.</div>
                </div>
                <div class="OneReight">
                  <img src="../../assets/img/cremaImg/icon2@2x.png" alt="">
                </div>
            </div>
            <div class="ThreeplugIn">
                <div class="Oneleft">
                    <div class="OneTop">Ready-To-Integrate DeFi Module</div>
                    <div class="OneBottom">The concentrated liquidity protocol of Crema can be easily integrated to any DAPPs in Solana ecosystem to aggregate the market depth.</div>
                </div>
                <div class="OneReight">
                  <img src="../../assets/img/cremaImg/icon3@2x.png" alt="">
                </div>
            </div>
        </div>
      </div>
      <!-- 横向插图区域 -->
      <div class="footerTop">
        <div class="footerTopAll">
            <div class="backGroundFour">
            <img src="../../assets/img/cremaImg/bg2@2x.png" alt="">
            </div>
            <div class="FooterBotto">
              <div class="footerTopOne">Roadmap</div>
              <div class="footerTopTwo">
                  <div class="dialogBoxLeft">
                    <div class="dialogBoxOne">2021 Oct</div>
                    <div class="dialogBoxTwo dialogBoxImg">
                        <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                        <span>Project Started</span>
                    </div>
                    <div class="dialogBoxThree dialogBoxImg">
                        <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                        <span>Seed Round Funding</span>
                    </div>
                    <div class="dialogBoxFour dialogBoxImg">
                        <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                        <span>MVP Version Launch</span>
                    </div>
                  </div>
                  <div class="addDialogBox"></div>
                  <div class="dialogBoxReight">
                    <div class="dialogBoxOne">2021 Dec</div>
                    <div class="dialogBoxTwo dialogBoxImg">
                        <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                        <span>Liquidity Farming</span>
                    </div>
                    <div class="dialogBoxThree dialogBoxImg">
                        <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                        <span>Cross-chain Use Case</span>
                    </div>
                    <div class="dialogBoxFour dialogBoxImg">
                        <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                        <span>User Experience Optimization</span>
                    </div>
                  </div>
              </div>
              <div class="footerTopThree">
                <img class="Oneball ball" src="../../assets/img/cremaImg/round-icon@2x.png" alt="">
                <img class="Twoball ball" src="../../assets/img/cremaImg/round-icon@2x.png" alt="">
                <img class="Threeball ball" src="../../assets/img/cremaImg/round-icon@2x.png" alt="">
                <img class="Fourball ball" src="../../assets/img/cremaImg/round-icon@2x.png" alt="">
                <img class="Line" src="../../assets/img/cremaImg/line@2x.png" alt="">
              </div>
              <div class="footerTopFour">
                  <div class="FourdialogBoxLeft">
                    <div class="dialogBoxReight">
                      <div class="dialogBoxOne">2021 Nov</div>
                      <div class="dialogBoxTwo dialogBoxImg">
                          <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                          <span>Strategic Round Funding</span>
                      </div>
                      <div class="dialogBoxThree dialogBoxImg">
                          <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                          <span>Official 1.0 Release</span>
                      </div>
                      <div class="dialogBoxFour dialogBoxImg">
                          <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                          <span>IDO & Fair Launch</span>
                      </div>
                    </div>
                  </div>
                  <div class="addDialogBox"></div>
                  <div class="FourdialogBoxReight">
                    <div class="dialogBoxReight">
                      <div class="dialogBoxOne">2022 Q1</div>
                      <div class="dialogBoxTwo dialogBoxImg">
                          <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                          <span>CLMM V2.0</span>
                      </div>
                      <div class="dialogBoxThree dialogBoxImg">
                          <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                          <span>vCRM Mint Function</span>
                      </div>
                      <div class="dialogBoxFour dialogBoxImg">
                          <img src="../../assets/img/cremaImg/biaotiyuan.png" alt="">
                          <span>DAO Platform</span>
                      </div>
                    </div>
                  </div>
              </div>
            </div>
        </div>
      </div>
      <!-- 底部 -->
      <div class="footer">
        <div class="footerMain">
          <div class="Left">
            <div class="LeftTopF">
              <img src="../../assets/img/cremaImg/logo@2x.png" alt="">
            </div>
            <div class="BottomText">© 2021 Crema. All rights reserved.</div>
          </div>
          <div class="Reight">
            <div class="ImgFooter">
              <img src="../../assets/img/cremaImg/twitter@2x.png" alt="">
              <img src="../../assets/img/cremaImg/telegram@2x.png" alt="">
              <img src="../../assets/img/cremaImg/medium@2x.png" alt="">
              <img src="../../assets/img/cremaImg/discord@2x.png" alt="">
            </div>
            <div class="BottomText"> hello@crema.finance</div>
          </div>
          <div class="backGroundFive">
            <img src="../../assets/img/cremaImg/cameloid9@2x.png" alt="">
          </div>
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
      showActive:1,
      localeList: [
        {
          label: "English",
          key: "en",
        },
        {
          label: "简体中文",
          key: "zh",
        }
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
  mounted() {
  },
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
    switchLanguage(lang,index) {
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
.outer{
  width: 100%;
  height: 100%;
  position: relative;
  .core{
    width: 100%;
    // background: url('../../assets/img/cremaImg/update.png') no-repeat;
    // background-size: cover;
    background: rgb(10, 9, 20);
    min-height:100vh;
    // display: flex;
    // justify-content: space-between;
    .header{
      height: 100px;
      line-height: 130px;
      width: 100%;
      // padding: 0 177px 0 178px;
      // display: flex;
      // justify-content: center;
      // text-align: center;
      .top{
        margin: 0 auto;
        height: 45px;
        width: 1200px;
        // width: 1940px;
        // padding: 0 300px 0 300px;
        display: flex;
        justify-content: space-between;
        .left{
          width: 200px;
          line-height: 143px;
          img{
            width: 162px;
            height: 45px;
          }
        }
        .reight{
          img{
            width: 24px;
            height: 24px;
          }
          .herderreightImg{
            margin-right: 20px;
          }
        }
      }
    }
    .main{
      // width: 1800px;
      width: 100%;
      height: 272px;
      // background: #000;
      // padding: 0 250px 0;
      // margin: 185px 0 0 -100px;
      margin: 185px 0 0 0;
      .mainAll{
        width: 1200px;
        display: flex;
        justify-content: space-between;
        margin: 0 auto;
        position: relative;
        .backGroundOne{
          position: absolute;
          z-index: 1;
          width: 415px;
          height: 224px;
          left: -18px;
          top: -10px;
          img{
            width: 415px;
            height: 224px;
          }
        }
        .mainReight{
          img{
            width: 346px;
            height: 400px;
            margin-top: -60px;
          }
        }
        video{
          // position: absolute;
          width: 346px;
          height: 400px;
          margin-top: -60px;
          // right: 400px;
          // top: 175px;
        }
        video::-webkit-media-controls-enclosure{
          display: none;
        }
        .mainLeft{
          .mainTop{
            padding: 0 0 0 0;
            span{
              line-height: 100px;
              font-size: 56px;
              font-weight: bold;
              color: #fff;
              background: linear-gradient(209deg,#59bdad 0%,#6676f5 62%,#eba7ff 100%);
              -webkit-background-clip: text;
              -webkit-text-fill-color: transparent;
              font-family: 'STYuanti-SC';
              position: absolute;
              z-index: 5;
            }
          }
          .mainCenter{
            margin-top: 10px;
            // padding: 0 0 0 247px;
            padding: 0 0 0 0 ;
            position: absolute;
            top: 100px;
            z-index: 4;
            span{
              color: #bababa;
              font-size: 26px;
              font-family: 'STYuanti-SC';
            }
          }
          .mainBottom{
            margin-top: 42px;
            // padding: 0 0 0 247px;
            padding: 0 0 0 0;
            display: flex;
            text-align: center;
            position: absolute;
            top: 170px;
            .BtnLeft{
              width: 148px;
              height: 48px;
              background: linear-gradient(209deg,#59bdad 0%,#6676f5 62%,#eba7ff 100%);
              border-radius: 22.5px;
              color: #fff;
              font-size: 14px;
              font-weight: bold;
              font-family: 'STYuanti-SC';
            }
            .BtnReight{
              display: none;
              margin-left: 20px;
              width: 100px;
              height: 48px;
              line-height: 48px;
              border-radius: 22.5px;
              background: url('../../assets/img/cremaImg/reightImgB.png') no-repeat;
              background-size: cover;
              color: #fff;
              font-size: 14px;
              font-family: 'STYuanti-SC';
              font-weight: bold;
            }
          }
        }
      }
    }
    .plugIn{
      // 154 44 150 40 164
      // width: 889px;
      width: 100%;
      height: 552px;
      margin: 165px 0 0 0;
      .plugInAll{
          width: 889px;
          margin: 0 auto;
          position: relative;
        .backGroundTwo{
          position: absolute;
          width: 485px;
          height: 484px;
          left: -130px;
          top: -150px;
        img{
            width: 485px;
            height: 484px;
          }
        }
        .backGroundThree{
          position: absolute;
          width: 485px;
          height: 484px;
          // left: 896px;
          // top: 915px;
          right: 0;
          bottom: -150px;
          img{
            width: 485px;
            height: 484px;
          }
        }
        .OneplugIn{
          width: 764px;
          height: 154px;
          background: url('../../assets/img/cremaImg/rectangle@2x.png') no-repeat;
          background-size: cover;
          padding: 20px 0 20px 20px;
          display: flex;
          justify-content: space-between;
          .Oneleft{
            width: 557px;
            display: flex;
            flex-wrap: wrap;
            .OneTop{
              font-size: 26px;
              width: 300px;
              font-weight: bold;
              color: #fff;
              font-family: 'STYuanti-SC';
            }
            .OneBottom{
              width: 557px;
              font-size: 16px;
              font-family: 'STYuanti-SC';
              color: #bababa;
            }
          }
          .OneReight{
            img{
              width: 226px;
              height: 86px;
            }
          }
        }
        .TwoplugIn{
          width: 764px;
          height: 154px;
          background: url('../../assets/img/cremaImg/rectangle@2x.png') no-repeat;
          background-size: cover;
          margin: 44px 0 0 125px;
          padding: 20px 0 20px 20px;
          display: flex;
          justify-content: space-between;
          .Oneleft{
            width: 557px;
            display: flex;
            flex-wrap: wrap;
            .OneTop{
              font-size: 26px;
              width: 300px;
              font-weight: bold;
              color: #fff;
              font-family: 'STYuanti-SC';
            }
            .OneBottom{
              width: 557px;
              font-size: 16px;
              color: #bababa;
              font-family: 'STYuanti-SC';
            }
          }
          .OneReight{
            img{
              width: 144px;
              height: 102px;
            }
          }
        }
        .ThreeplugIn{
          width: 764px;
          height: 154px;
          background: url('../../assets/img/cremaImg/rectangle@2x.png') no-repeat;
          background-size: cover;
          margin: 40px 0 0 0;
          padding: 20px 0 20px 20px;
          display: flex;
          justify-content: space-between;
          .Oneleft{
            width: 557px;
            display: flex;
            flex-wrap: wrap;
            .OneTop{
              font-size: 26px;
              width: 250px;
              font-weight: bold;
              color: #fff;
              font-family: 'STYuanti-SC';
            }
            .OneBottom{
              width: 557px;
              font-size: 16px;
              color: #bababa;
              font-family: 'STYuanti-SC';
            }
          }
          .OneReight{
            img{
              width: 121px;
              height: 121px;
            }
          }
        }
      }

    }
    .footerTop{
        height: 540px;
        // width: 901px;
        width: 100%;
        // background: #000;
        margin: 118px 0 0 0;
        text-align: center;
        position: relative;
        .footerTopAll{
          width: 901px;
          margin: 0 auto;
          position: relative;
          .backGroundFour{
            position: absolute;
            width: 110px;
            height: 117px;
            left: 392px;
            top: -30px;
            img{
              width: 110px;
              height: 117px;
            }
          }
          .FooterBotto{
            position: absolute;
            .footerTopOne{
              margin: 0 auto;
              font-weight: bold;
              color: #fff;
              font-size: 36px;
              font-family: 'STYuanti-SC';
            }
            // 616 178 224 214
            .footerTopTwo{
              width: 616px;
              height: 148px;
              margin-top: 73px;
              display: flex;
              justify-content: space-between;
              .dialogBoxLeft{
                width: 178px;
                height: 148px;
                background: url('../../assets/img/cremaImg/shapeCombination@2x(4).png') no-repeat;
                background-size: cover;
                .dialogBoxImg{
                  margin: 5px 0 0 -44px;
                  img{
                    width: 6px;
                    height: 6px;
                    margin-right: 4px;
                  }
                  span{
                    font-size: 14px;
                    color: #bababa;
                    font-family: 'STYuanti-SC';
                  }
                }
                .dialogBoxOne{
                  padding: 16px 21px 0 16px;
                  margin-left: -40px;
                  color: #fff;
                    font-family: 'STYuanti-SC';
                  font-weight: bold;
                  font-size: 24px;
                }
                .dialogBoxThree{
                  margin-left: -8px;
                }
                .dialogBoxFour{
                  margin-left: -11px;
                }
              }
              .dialogBoxReight{
                width: 224px;
                height: 148px;
                background: url('../../assets/img/cremaImg/shapeCombination@2x(1).png') no-repeat;
                background-size: cover;
                .dialogBoxImg{
                  margin: 5px 0 0 -80px;
                  img{
                    width: 6px;
                    height: 6px;
                    margin-right: 4px;
                  }
                  span{
                    font-size: 14px;
                    color: #bababa;
                    font-family: 'STYuanti-SC';
                  }
                }
                .dialogBoxOne{
                  padding: 16px 21px 0 16px;
                  margin-left: -80px;
                  color: #fff;
                    font-family: 'STYuanti-SC';
                  font-weight: bold;
                  font-size: 24px;
                }
                .dialogBoxThree{
                  margin-left: -50px;
                }
                .dialogBoxFour{
                  margin-left: 0px;
                }
              }
            }
            .footerTopThree{
              position: relative;
              .ball{
                position: absolute;
                width: 25px;
                height: 24px;
                // margin-bottom: 20px;
                // top: 272px;
              }
              .Oneball{
                left: 140px;
              }
              .Twoball{
                left: 332px;
              }
              .Threeball{
                left: 572px;
              }
              .Fourball{
                left: 750px;
              }
              .Line{
                width: 901px;
                height: 3px;
              }
            }
            .footerTopFour{
              width: 615px;
              height: 149px;
              margin-left: 180px;
              margin-top: 12px;
              display: flex;
              justify-content: space-between;
              .FourdialogBoxLeft{
                width: 194px;
                height: 149px;
                background: url('../../assets/img/cremaImg/shapeCombination@2x(3).png') no-repeat;
                background-size: cover;
                .dialogBoxImg{
                  margin: 5px 0 0 7px;
                  img{
                    width: 6px;
                    height: 6px;
                    margin-right: 4px;
                  }
                  span{
                    font-size: 14px;
                    color: #bababa;
                    font-family: 'STYuanti-SC';
                  }
                }
                .dialogBoxOne{
                  padding: 16px 21px 0 16px;
                  margin: 10px 0 0 -40px;
                  color: #fff;
                  font-family: 'STYuanti-SC';
                  font-weight: bold;
                  font-size: 24px;
                }
                .dialogBoxThree{
                  margin-left: -37px;
                }
                .dialogBoxFour{
                  margin-left: -41px;
                }
              }
              .FourdialogBoxReight{
                width: 194px;
                height: 149px;
                background: url('../../assets/img/cremaImg/shapeCombination@2x(3).png') no-repeat;
                background-size: cover;
                .dialogBoxImg{
                  margin: 5px 0 0 -80px;
                  img{
                    width: 6px;
                    height: 6px;
                    margin-right: 4px;
                  }
                  span{
                    font-size: 14px;
                    color: #bababa;
                    font-family: 'STYuanti-SC';
                  }
                }
                .dialogBoxOne{
                  padding: 16px 21px 0 16px;
                  margin: 10px 0 0 -40px;
                  color: #fff;
                  font-family: 'STYuanti-SC';
                  font-weight: bold;
                  font-size: 24px;
                }
                .dialogBoxThree{
                  margin-left: -20px;
                }
                .dialogBoxFour{
                  margin-left: -63px;
                }
              }
            }
          }

        }

    }
    .footer{
      width: 100%;
      height: 107px;
      line-height: 43px;
      .footerMain{
        width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        border-top: 1px solid #494949;
        padding-top: 20px;
        position: relative;
        .backGroundFive{
          position: absolute;
          width: 504px;
          height: 262px;
          left: 7px;
          bottom: 0px;
          img{
            width: 504px;
            height: 262px;
          }
        }
        .Left{
          .LeftTopF{
            img{
              width: 87px;
              height: 24px;
            }
          }
          .BottomText{
            color: #fff;
            font-size: 14px;
            opacity: 0.8;
          }
        }
        .Reight{
          img{
            width: 24px;
            height: 24px;
            margin-left: 7px;
          }
          .BottomText{
            color: #fff;
            font-size: 14px;
            opacity: 0.8;
          }
        }
      }
    }
  }
}
@keyframes bounce-down {
        25% {
             transform: translateY(-4px);
        }
        50%, 100% {
             transform: translateY(0);
        }
        75% {
             transform: translateY(4px);
        }
}
@keyframes bounce-opcity {
        25% {
             opacity: 0.5;
        }
        // 40%{
        //      opacity: 0.3;
        // }
        50%{
             opacity: 0;
        }
        75% {
             opacity: 0.5;
        }
        // 75% {
        //      opacity: 0.9;
        // }
        100% {
             opacity: 1.0;
        }
}
@media screen and (max-width: 750px) {
  .outer{
    .core{
      .header{
        // display: none;
        height: 30px;
        width: 100%;
        line-height: 46px;
        // width: 375px;
        .top{
          // display: none;
          width: 340px;
          padding: 17px 0 0;
          .left{
            line-height: 0;
            width: 108px;
            img{
              width: 108px;
              height: 30px;
            }
          }
          .reight{
            img{
              width: 24px;
              height: 24px;
            }
            .herderreightImg{
              margin-right: 10px;
            }
          }
        }
      }

      .main{
        // display: none;
        // width: 500px;
        width: 100%;
        margin:50px 0 0 0;
        .mainAll{
          // display: none;
          width: 360px;
          height: 500px;
          // background: #bfa;
          margin: 0 auto;
          position: relative;
          display: flex;
          flex-wrap: wrap;
          .backGroundOne{
            // display: none;
            width: 334px;
            height: 180px;
            left: -20px;
            top: 40px;
            img{
              width: 378px;
              height: 200px;
            }
          }
          .mainReight{
              width: 236px;
              height: 273px;
              margin: 300px 0 0 65px;
              position: absolute;
          }
          video{
            // display: none;
            width: 236px;
            height: 273px;
            margin: 300px 0 0 65px;
            position: absolute;

            // top: 380px;
            // left: 180px;
          }
          .mainLeft{
            // display: none;
            .mainTop{
              // padding: 0 0 0 156px;
              margin: 90px 0 0 28px;
              span{
                font-size: 36px;
              }
            }
            .mainCenter{
              // padding: 0 0 0 156px;
              margin: 80px 0 0 28px ;
              span{
                font-size: 16px;
              }
            }
            .mainBottom{
              // padding: 0 0 0 156px;
              margin: 80px 0 0 28px;
              span{
                font-size: 14px;
              }
            }
          }
        }

      }
      .plugIn{
        // display: none;
        width: 335px;
        // width: 100px;
        height: 100%;
        margin: 320px 0 0 0;
        .plugInAll{
          // display: none;
          width: 300px;
          height: 100%;
          margin-left: 20px;
          .backGroundTwo{
            // display: none;
            left: -200px;
          }
          .backGroundThree{
            // display: none;
          }
          .OneplugIn{
            width: 335px;
            height: 230px;
            background: url('../../assets/img/cremaImg/h5juxing.png') no-repeat;
            background-size: cover;
            padding: 0 19px 22px 16px;
            display: flex;
            flex-wrap: wrap;
            position: relative;
            // margin-left: 150.5px;
            .Oneleft{
              height: 138px;
              width: 300px;
              margin-top: 70px;
              .OneTop{
                font-size: 24px;
              }
              .OneBottom{
                font-size: 14px;
              }
            }
            .OneReight{
              position: absolute;
              right: 10px;
              img{
                width: 159px;
                height: 60px;
              }
            }
          }
          .TwoplugIn{
            width: 335px;
            height: 230px;
            background: url('../../assets/img/cremaImg/h5juxing.png') no-repeat;
            background-size: cover;
            padding: 0 19px 22px 16px;
            margin: 30px 0 0 0;
            display: flex;
            flex-wrap: wrap;
            position: relative;
            // margin-left: 150.5px;
            .Oneleft{
              height: 138px;
              width: 300px;
              margin-top: 70px;
              .OneTop{
                font-size: 24px;
              }
              .OneBottom{
                font-size: 14px;
              }
            }
            .OneReight{
              position: absolute;
              right: 10px;
              img{
                width: 104px;
                height: 74px;
              }
            }
          }
          .ThreeplugIn{
            // display: none;
            width: 335px;
            height: 230px;
            margin: 30px 0 0 0;
            background: url('../../assets/img/cremaImg/h5juxing.png') no-repeat;
            background-size: cover;
            padding: 0 19px 22px 16px;
            display: flex;
            flex-wrap: wrap;
            position: relative;
            // margin-left: 150.5px;
            .Oneleft{
              height: 138px;
              width: 300px;
              margin-top: 70px;
              .OneTop{
                font-size: 24px;
              }
              .OneBottom{
                font-size: 14px;
              }
            }
            .OneReight{
              position: absolute;
              right: 10px;
              img{
                width: 94px;
                height: 94px;
              }
            }
          }
        }
      }
      .footerTop{
        // display: none;
        margin: 0 0 0 -40px;
        width: 337px;
        height: 900px;
        position: relative;
        .footerTopAll{
          width: 337px;
          height: 900px;
          .backGroundFour{
            // display: none;
            left: 165px;
            top: 20px;
          }
          .FooterBotto{
            .footerTopOne{
              margin: 50px 0 0 65px;
            }
            .footerTopTwo{
              width: 340px;
              flex-wrap: wrap;
              height: 100%;
              margin-left: 40px;

              .dialogBoxLeft{
                // margin-left: 16px;
                position: absolute;
                left: 100px;
                top: 147px;
                width: 190px;
                height: 134px;
                background: url('../../assets/img/cremaImg/Onecline.png') no-repeat;
                background-size: cover;
                .dialogBoxImg{
                  margin: 5px 0 0 -20px;
                  img{
                    width: 6px;
                    height: 6px;
                    margin-right: 4px;
                  }
                  span{
                    font-size: 14px;
                    color: #bababa;
                    font-family: 'STYuanti-SC';
                  }

                }
                .dialogBoxOne{
                  padding: 16px 21px 0 44px;
                  margin-left: -40px;
                  color: #fff;
                  font-family: 'STYuanti-SC';
                  font-weight: bold;
                  font-size: 24px;
                }
                .dialogBoxThree{
                  margin-left: 17px;
                }
                .dialogBoxFour{
                  margin-left: 15px;
                }
              }
              .addDialogBox{
                width: 25px;
                height: 704px;
                background: url('../../assets/img/cremaImg/topLine.png') no-repeat;
                background-size: cover;
                // margin-left: 20px;
                position: absolute;
                left: 69px;
                top: 100px;
              }
              .dialogBoxReight{
                width: 265px;
                height: 150px;
                position: absolute;
                background: url('../../assets/img/cremaImg/Threecline.png') no-repeat;
                background-size: cover;
                top: 468px;
                left: 100px;
                .dialogBoxImg{
                  margin: 5px 0 0 -70px;
                  img{
                    width: 6px;
                    height: 6px;
                    margin-right: 4px;
                  }
                  span{
                    font-size: 14px;
                    color: #bababa;
                    font-family: 'STYuanti-SC';
                  }

                }
                .dialogBoxOne{
                  padding: 16px 21px 0 8px;
                  margin-left: -40px;
                  color: #fff;
                  font-family: 'STYuanti-SC';
                  font-weight: bold;
                  font-size: 24px;
                }
                .dialogBoxThree{
                  margin-left: -40px;
                }
                .dialogBoxFour{
                  margin-left: 11px;
                }
              }
            }
            .footerTopThree{
              display: none;
            }
            .footerTopFour{
              width: 340px;
              flex-wrap: wrap;
              margin-left: 40px;
              // display: none;
              .FourdialogBoxLeft{
                position: absolute;
                left: 100px;
                top: 300px;
                width: 230px;
                height: 150px;
                background: url('../../assets/img/cremaImg/Twocline.png') no-repeat;
                background-size: cover;
                .dialogBoxOne{
                  padding: 16px 21px 0 37px;
                  margin-left: -40px;
                  color: #fff;
                  font-family: 'STYuanti-SC';
                  font-weight: bold;
                  font-size: 24px;
                }
                .dialogBoxImg{
                  margin: 5px 0 0 7px;
                  img{
                    width: 6px;
                    height: 6px;
                    margin-right: 4px;
                  }
                  span{
                    font-size: 14px;
                    color: #bababa;
                    font-family: 'STYuanti-SC';
                  }
                }
                .dialogBoxThree{
                  margin-left: -36px;
                }
                .dialogBoxFour{
                  margin-left: -38px;
                }
              }
              .addDialogBox{
                display: none;
                position: absolute;
                top: 658px;
                left: 84px;
                width: 337px;
                height: 24px;
                background: url('../../assets/img/cremaImg/bianzu@2x.png') no-repeat;
                background-size: cover;
                margin-left:-21.5px;
              }
              .FourdialogBoxReight{
                // display: none;
                position: absolute;
                top: 638px;
                left: 100px;
                width: 236px;
                height: 134px;
                background: url('../../assets/img/cremaImg/Fourcline.png') no-repeat;
                background-size: cover;
                .dialogBoxOne{
                  padding: 5px 21px 0 0px;
                  color: #fff;
                  font-family: 'STYuanti-SC';
                  font-weight: bold;
                  font-size: 24px;
                }
                .dialogBoxImg{
                  margin: 5px 0 0 -85px;
                  img{
                    width: 6px;
                    height: 6px;
                    margin-right: 4px;
                  }
                  span{
                    font-size: 14px;
                    color: #bababa;
                    font-family: 'STYuanti-SC';
                  }

                }
                .dialogBoxThree{
                  margin-left: -27px;
                }
                .dialogBoxFour{
                  margin-left: -68px;
                }

              }
            }
          }

        }
      }
      .footer{
        // display: none;
        height: 178px;
        width: 100%;
        line-height: 20px;
        position: relative;
        .footerMain{
          flex-wrap: wrap;
          width: 360px;
          padding: 0 0 0 0;
          .backGroundFive{
            display: none;
            bottom: -178px;
            left: -120px;
          }
          .Left{
            // display: none;
            width: 300px;
            .LeftTopF{
              position: absolute;
              left: 10px;
              top: 20px;
            }
            .BottomText{
              position: absolute;
              left: 10px;
              top: 120px;
            }
          }
          .Reight{
            // display: none;
            .ImgFooter{
              position: absolute;
              left: 0px;
              top: 60px;
            }
            .BottomText{
              position: absolute;
              left: 10px;
              top: 90px;
            }
          }
        }
      }
    }
  }
}
</style>
