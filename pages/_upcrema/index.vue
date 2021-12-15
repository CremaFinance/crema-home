<template>
  <div class="outer">
    <!-- 头部导航栏区域 -->
    <div class="header">
      <div class="navLeft">
        <img src="../../assets/img/cremaWebImg/headerLogo.png">
      </div>
      <div class="navReight">
        <a href="https://beta.crema.finance/" target="_blank">Beta APP</a>
        <div>
          <a href="https://twitter.com/Crema_Finance" target="_blank"></a>
          <a href="https://t.me/cremafinance" target="_blank"></a>
          <a href="https://medium.com/@Crema.finance" target="_blank"></a>
          <a href="https://discord.gg/hCaFmvvPYH" target="_blank"></a>
        </div>
      </div>
    </div>
    <!-- 主体区域 -->
    <div class="main" :class="faqVal ? 'mainBig':''">
      <div class="top">
        <!-- <img src="../../assets/img/cremaWebImg/cremaHeader.png" alt=""> -->
          <div></div>
          <div><a href="https://beta.crema.finance/" target="_blank">Beta APP</a></div>
      </div>
      <div class="center">
        <div class="botTop">
          <span>Core Products</span>
          <!-- <img src="../../assets/img/cremaWebImg/cremaTitlea.png" alt=""> -->
        </div>
        <div class="centerTop centerAll">
          <div class="centerTopLeft">
            <div class="Conce">Concentrated Liquidity Market Maker</div>
            <div class="CLMM">CLMM allows liquidity providers to set specific price ranges and add single-sided liquidity. It will redefine the capital efficiency and trading depth on Solana.</div>
          </div>
        </div>
        <div class="centerMain centerAll">
          <div class="centerTopLeft">
            <div class="Conce">LP NFT Farming</div>
            <div class="CLMM">A special gift from Crema. The non-fungible liquidity contributed by liquidity providers are eligible to earn extra rewards from Crema's LP NFT Farming. </div>
          </div>
        </div>
        <div class="centerBottom centerAll">
          <div class="centerTopLeft">
            <div class="Conce">Integrated Aggregators</div>
            <div class="CLMM">Crema is mutually integrated with influential aggregators on Solana such as Jupiter, which helps all users to easily access the full liquidity within the ecosystem. </div>
          </div>
        </div>
      </div>
      <div class="edges" @mouseover="changeOff()" @mouseleave="changeGo()">
        <div class="botTop">
          <span>Our Edges</span>
          <!-- <img src="../../assets/img/cremaWebImg/cremaTitlea.png" alt=""> -->
        </div>
         <div class="edgesAll">
          <div class="edgesLeft">
            <div class="Conce">{{this.num==1 ? this.changeone.top : this.num==2 ? this.changetwo.top : this.num==3 ? this.changethree.top : this.changefour.top}}</div>
            <div class="CLMM">{{this.num==1 ? this.changeone.bto : this.num==2 ? this.changetwo.bto : this.num==3 ? this.changethree.bto : this.changefour.bto}}</div>
            <div class="edgesBtn">
              <div :class="this.num == 1 ? 'btnSize':''" @click="cutEle(1)"></div>
              <div :class="this.num == 2 ? 'btnSize':''" @click="cutEle(2)"></div>
              <div :class="this.num == 3 ? 'btnSize':''" @click="cutEle(3)"></div>
              <div :class="this.num == 4 ? 'btnSize':''" @click="cutEle(4)"></div>
            </div>
          </div>
          <div class="edgesRight" 
              :class="num == 1 ? 'eone' :
              num == 2 ? 'etwo' : 
              num == 3 ? 'ethree' : 'efour'"></div>
        </div>
      </div>
      <div class="Roadmap">
        <div class="botTop">
          <span>Roadmap</span>
          <!-- <img src="../../assets/img/cremaWebImg/cremaTitlea.png" alt=""> -->
        </div>
         <div class="RoadmapAll">
           <div>
             <div>
               <span>Project Started</span>
               <span>R&D Started</span>
               <span>Devnet Beta Release</span>
             </div>
             <div>
               <span>TGE & IDO Event</span>
               <div>
                  <span>MVP Release</span>
                  <div @click="changeJan" :class="isJan ? 'jancla':''"></div>
               </div>
               <p v-for="item in janForm" v-if="isJan">{{item.val}}</p>
             </div>
             <div>
               <!-- <span>CLMM V2</span> -->
               <div>
                  <span>CLMM V2</span>
                  <div @click="changeq" :class="isq ? 'jancla':''"></div>
               </div>
               <p style="width:190px;" v-for="item in qForm" v-if="isq">{{item.val}}</p>
               <span>Cross Chain Swap</span>
             </div>
           </div>
           <div>
             <div>
               <span>2021 Nov</span>
               <span>2022 Jan</span>
               <span>2022 Q2</span>
             </div>
             <div></div>
             <div>
               <span>2021 Dec</span>
               <span>2022 Feb-Mar</span>
             </div>
           </div>
           <div>
             <div>
               <!-- <span>Mainnet Beta Release</span> -->
               <div>
                  <span>Mainnet Beta Release</span>
                  <div @click="changedec" :class="isdec ? 'jancla':''"></div>
               </div>
               <p style="width:190px;" v-for="item in decForm" v-if="isdec">{{item.val}}</p>
               <!-- <span>Integrate with Aggregators</span> -->
               <div>
                  <span>Integrate with Aggregators</span>
                  <div @click="changeint" :class="isint ? 'jancla':''"></div>
               </div>
               <p v-for="item in intForm" v-if="isint">{{item.val}}</p>
             </div>
             <div>
               <!-- <span>DAO Platform Started</span> -->
               <div>
                  <span>DAO Platform Started</span>
                  <div @click="changemar" :class="ismar ? 'jancla':''"></div>
               </div>
               <p style="width:190px;" v-for="item in marForm" v-if="ismar">{{item.val}}</p>
               <span>Liquidity Migration</span>
               <span>Liquidity Bridge</span>
             </div>
           </div>
        </div>
        <div></div>
      </div>
      <div class="bottom" :class="faqVal ? 'bottomBig':''">
        <div class="botTop">
          <span>FAQ</span>
          <!-- <img src="../../assets/img/cremaWebImg/cremaTitlea.png" alt=""> -->
        </div>
        <div class="botBto" v-for="item in faqForm"  @click="faqText(item)">
          <div>
            <span :class="item.ccp ? 'cftcy':''">{{item.value}}</span>
            <div :class="faqVal == item.child ? 'change' : ''"></div>
          </div>
          <div v-if="faqVal == item.child">
            <span>{{item.child}}</span>
          </div>
        </div>
      </div>
    </div>
    <!-- 底部区域 -->
    <div class="footer">
      <div class="footerAll">
        <div>
          <img src="../../assets/img/cremaWebImg/footerLogo.png" alt="">
          <div class="ReiImg">
            <a href="https://twitter.com/Crema_Finance" target="_blank"></a>
            <a href="https://t.me/cremafinance" target="_blank"></a>
            <a href="https://medium.com/@Crema.finance" target="_blank"></a>
            <a href="https://discord.gg/hCaFmvvPYH" target="_blank"></a>
          </div>
        </div>
        <div>
          <div>
            <p>Cooperate & Invest</p>
            <p>bd@crema.finance</p>
            <!-- <a href="##" ref="copya" @click="copy('a')"></a> -->
          </div>
          <div>
            <p>General Inquiries</p>
            <p>hello@crema.finance</p>
            <!-- <a href="##" ref="copy" @click="copy('b')"></a> -->
          </div>
        </div>
        <div>
            <p>© 2021 Crema. All rights reserved.</p>
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
      showActive: 1,
      screenWidth: '',
      screenHeight: '',
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
      faqVal:'',
      faqForm:[
        {
          value:'1. What kind of product is Crema?',
          child:"Crema Finance is a powerful concentrated liquidity protocol on Solana. The core product delivered by Crema is its concentrated liquidity market maker, which is a fully augmented algorithm to drive decentralized trading. Liquidity providers can add liquidity on Crema within specific price ranges that they target; Traders can easily place swap orders with much lower price slippage; Developers can integrate Crema's service to enrich their Dapps and build a stronger DeFi. Moreover, Crema Finance also provides a series of creative features to serve its users better such as LP NFT Farming, integrated aggregators, etc."
        },{
          value:'2. What key issues does Crema aim to solve?',
          child:'Everything we do is ultimately for one goal: to enhance the overall capital efficiency on Solana to the next level. During this process, many common headaches that DeFi users have right now will be solved such as high impermanent loss, large price slippage, etc.'
        },{
          value:'3. What is CLMM?',
          child:'CLMM means concentrated liquidity market maker. It can be used by DEX platforms to drive its decentralized trading. With CLMM, liquidity providers can set specific price ranges for the liquidity they add. Therefore, users can utilize CLMM to make transactions more precisely and efficiently by conducting range orders, which is as efficient and flexible as limit order trading on centralized exchanges.',
          ccp:3,
        },{
          value:'4. Why is CLMM a superior model compared with AMM?',
          child:"In AMM model, only the liquidity close to the real-time trading price will be utilized, which means most of the capital contributed by liquidity providers are remaining unused in long term. This is definitely a waste of resources. Instead, in CLMM, liquidity providers can set specific price ranges in which they want their liquidity to be traded. As most liquidity providers tend to add liquidity around the current market price, this naturally increases the near-market-price liquidity depth. It does not only enhance CLMM trading pools' resilience to the selling pressure but also largely improves liquidity providers' capital efficiency."
        },{
          value:'5. Why should I provide liquidity on Crema?',
          child:"For liquidity providers, now you can fully control the price range of your liquidity positions and you will never suffer from impermanent loss any more. The liquidity you add on Crema will perform higher efficiency than anywhere else on fee earning because your liquidity is more focused within the price curve. These should be enough for most liquidity providers to make the decision. What's more? You can also earn high-APR extra rewards from LP NFT Farming, which is the exclusive offer from Crema."
        },{
          value:'6. Why should I choose Crema to swap?',
          child:"On Crema, the price slippage of your order will be much lower than that of those AMM platforms, because the liquidity added by liquidity providers are more concentrated around the market price, which means the market depth is better here. Besides, Crema will integrate aggregators into its protocol, which will always detect the best price throughout the entire Solana ecosystem for you."
        },{
          value:'7. Will Crema support liquidity mining in future?',
          child:"Yes, absolutely. Since the CLMM liquidity providers on Crema are receiving NFT(non-fungible token) instead of the common fungible LP tokens, it is actually challenging for CLMM to support liquidity mining. However, Crema has already got its plan. It will launch its LP NFT farming function soon after its MVP launch. Extra incentives will be rewarded to liquidity providers fairly and precisely according to the effective value of their liquidity positions. Besides, general staking and LP farming will also be supported."
        },{
          value:'8. Any valuable utilities for $CRM token?',
          child:"There are three major token utilities for Crema, which namely are staking, boosting and governance. Users could stake CRM to get vCRM and vCRM owners could not only earn a cut from Crema's transaction fee revenue, but can also trigger other utilities. They can use vCRM to boost their liquidity mining APR or to vote and make proposals through the DAO."
        },{
          value:'9. Which wallets are accessible to Crema?',
          child:"Crema supports all mainstream Solana wallets, such as Phantom, Sollet, Solong, etc. If you don't have a Solana wallet previously, then Phantom Wallet is recommended. You can install its Web3 plugin to your browser and top it up with some SOL balance before accessing Crema."
        },
      ],
      isJan:false,
      janForm:[
        {
          val:'NFT Liquidity Farming'
        },
        {
          val:'LAAS (Liquidity as as Service)'
        }
      ],
      isq:false,
      qForm:[
        {
          val:'Discretized Liquidity'
        },
        {
          val:'Limit Order'
        }
      ],
      isdec:false,
      decForm:[
        {
          val:'CLMM'
        },
        {
          val:'Range Order'
        },
        {
          val:'Add/Remove Liquidity'
        }
      ],
      ismar:false,
      marForm:[
        {
          val:'vCRM Stake & Mint'
        },
        {
          val:'Proposal & Voting'
        },
        {
          val:'Boosting'
        }
      ],
      isint:false,
      intForm:[
        {
          val:'Integrate CLMM Pool to Aggregators'
        },
        {
          val:'Integrate Aggregator to Crema Swap'
        }
      ],

      num:1,
      changeone:{
        top:'Unparalleled Capital Efficiency',
        bto:'CLMM delivers 10-50x higher capital efficiency than the common AMM model does on Solana. '
      },
      changetwo:{ 
        top:'Aggregated by Powerful Ones',
        bto:'Crema has reached strategic partnerships with influential players on the stage such as Jupiter, Mercurial, etc., and the exploration will never stop.'
      },
      changethree:{
        top:'Multiple Incentives',
        bto:'Powered by the better fee earning  capability and LP NFT farming, Crema gives best incentives to liquidity providers.'
      },
      changefour:{
        top:'A Core DeFi Building Block',
        bto:"Crema's liquidity protocol is fully integratable to different Dapps, which is your key to the DeFi 2.0 on Solana."
      },
      // locale: "简体中文",
      timer: '',
      value: 0
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
    // 定时器开启
    this.timer = setInterval(this.get, 5000);
    this.screenWidth = document.body.clientWidth;
    this.screenHeight = document.body.clientHeight;
    window.onresize = () => {
      return (() => {
        this.screenWidth = document.body.clientWidth;
        this.screenHeight = document.body.clientHeight;
      })();
    };
  },
  beforeDestroy() {
    clearInterval(this.timer);
  },
  methods: {
    changeJan(){
      this.isJan = !this.isJan;
    },
    changeq(){
      this.isq = !this.isq;
    },
    changedec(){
      this.isdec = !this.isdec;
    },
    changemar(){
      this.ismar = !this.ismar;
    },
    changeint(){
      this.isint = !this.isint;
    },
    
    // 当鼠标移入时关闭定时器
    changeOff(){
      clearInterval(this.timer);
    },
    // 当鼠标移出时开启定时器
    changeGo(){
      this.timer = setInterval(this.get, 5000);
    },
    get() {
      this.num ++;
      if(this.num == 5){
        this.num = 1;
      }
    },
    cutEle(val){
      if(val == 1){
        this.num = 1;
      }
      if(val == 2){
        this.num = 2;
      }
      if(val == 3){
        this.num = 3;
      }
      if(val == 4){
        this.num = 4;
      }
    },
    faqText(e){
      if(this.faqVal && this.faqVal == e.child){
        this.faqVal = '';
        return;
      }
      this.faqVal = e.child;
    },
    copy(e){
      if(e == 'a'){
        let text = this.$refs.copya.previousSibling.previousSibling;
        const selection = window.getSelection();
        if(selection.rangeCount > 0) selection.removeAllRanges();
        const range = document.createRange();
        range.selectNodeContents(text);
        selection.addRange(range);
        document.execCommand("copy");
      }else{
        let text = this.$refs.copy.previousSibling.previousSibling;
        const selection = window.getSelection();
        if(selection.rangeCount > 0) selection.removeAllRanges();
        const range = document.createRange();
        range.selectNodeContents(text);
        selection.addRange(range);
        document.execCommand("copy");
      }
      
    },
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
  watch:{
    screenWidth(){
      if(this.screenWidth<=750){
        this.isJan = true;
        this.isq = true;
        this.isdec = true;
        this.ismar = true;
        this.isint = true;
      }
      if(this.screenWidth>750){
        this.isJan = false;
        this.isq = false;
        this.isdec = false;
        this.ismar = false;
        this.isint = false;
      }
    }
  }
};
</script>
<style lang="scss" scoped>

.outer {
  width: 100%;
  height: 100%;
  background: #14191E;
  position: relative;
  font-family: 'SansSerifExbFLF';
  .header {
    width: 1000px;
    height: 115px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 auto;
    position: relative;
    z-index: 100;
    .navLeft{
      width: 180px;
      height: 43px;
      img{
        // width: 180px;
        // height: 43px;
        width: 160px;
        height: 36px;
      }
    }
    .navReight{
      height: 46px;
      width: 338px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      > a{
        display: block;
        width: 138px;
        height: 46px;
        background-image: url('../../assets/img/cremaWebImg/buttonHeadc.png');
        background-size: 100% 100%;
        cursor: pointer;
        font-size: 12px;
        padding: 16px 40px;
        color: #fff;
        font-family: 'Montserrat-Bold';
      }
      > a:hover{
        background-image: url('../../assets/img/cremaWebImg/HoverbuttonHeadc.png');
      }
      > div{
        width: 170px;
        height: 20px;
        display: flex;
        justify-content: space-between;
        a{
          display: block;
          width: 20px;
          height: 20px;
          background-size: 100% 100%;
        }
        > a:nth-child(1){
          background-image: url('../../assets/img/cremaWebImg/icon_twitter@2x.png');
        }
        > a:nth-child(1):hover{
          background-image: url('../../assets/img/cremaWebImg/icon_twitter.png');
        }
        > a:nth-child(2){
          background-image: url('../../assets/img/cremaWebImg/icon_TelegramGroup@2x.png');
        }
        > a:nth-child(2):hover{
          background-image: url('../../assets/img/cremaWebImg/icon_TelegramGroup.png');
        }
        > a:nth-child(3){
          background-image: url('../../assets/img/cremaWebImg/icon_Medium@2x.png');
        }
        > a:nth-child(3):hover{
          background-image: url('../../assets/img/cremaWebImg/icon_Medium.png');
        }
        > a:nth-child(4){
          background-image: url('../../assets/img/cremaWebImg/icon_Discord@2x.png');
        }
        > a:nth-child(4):hover{
          background-image: url('../../assets/img/cremaWebImg/icon_Discord.png');
        }
      }
    }
  }
  .main{
    width: 100%;
    // height: 5205px;
    height: 4750px;
    padding: 10px 0 0 0;
    font-family: 'SansSerifExbFLF';
    .top{
      height: 1050px;
      width: 100%;
      display: flex;
      justify-content: center;
      margin: 0 auto;
      position: relative;
      > div:nth-child(1){
        // background-image: url('../../assets/img/cremaWebImg/cremaHeader.png');
        background-image: url('../../assets/img/cremaWebImg/newHeader.png');
        // background-image: url('../../assets/img/cremaWebImg/cremaImgheader.png');
        background-size: 100% 100%;
        width: 1400px;
        // height: 73%;,
        height: 78%;
        // width: 1300px;
        // height: 905px;
        margin-top: -90px;
        z-index: 1;
      }
      > div:nth-child(2){
          position: absolute;
          z-index: 20;
          width: 100%;
          // top: 480px;
          top: 520px;
          display: flex;
          justify-content: center;
        > a{
          // position: absolute;
          // z-index: 20;
          // left: 445px;
          font-family: 'Montserrat-Bold';
          width: 210px;
          height: 70px;
          background-image: url('../../assets/img/cremaWebImg/buttonHeadc.png');
          background-size: 100% 100%;
          font-size: 24px;
          color: #fff;
          padding: 20px 48px;
        }
        > a:hover{
          background-image: url('../../assets/img/cremaWebImg/HoverbuttonHeadc.png');
        }
      }
    }
    .center{
      height: 1550px;
      width: 100%;
      margin-top: -320px;
      .botTop{
        width: 1200px;
        height: 150px;
        line-height: 150px;
        margin: 0 auto;
        color: #fff;
        font-size: 28px;
        font-family: 'SansSerifExbFLF';
        display: flex;
        justify-content: center;
        img{
          width: 150px;
          height: 70px;
        }
      }
      .centerAll{
        // width: 1200px;
        // height: 460px;
        width: 1000px;
        height: 420px;
        padding: 0 0 0 40px;
        margin: 0 auto;
        border-radius: 30px;
        .centerTopLeft{
          // width: 450px;
          // width: 410px;
          width: 370px;
          height: 460px;
          // padding: 120px 0 116px;
          padding: 100px 0 116px;
          margin: auto 0;
          .Conce{
            font-size: 20px;
            font-family: 'Montserrat-Bold';
            color: #fff;
          }
          .CLMM{
            margin-top: 40px;
            color: #959CAC;
            font-size: 18px;
            line-height: 36px;
            font-family: 'Avenir';
          }
        }
      }
      .centerTop{
        background-image: url('../../assets/img/cremaWebImg/textTop.png');
        background-size: 100% 100%;
      }
      .centerMain{
        margin-top: 60px;
        background-image: url('../../assets/img/cremaWebImg/textMain.png');
        background-size: 100% 100%;
      }
      .centerBottom{
        margin-top: 60px;
        background-image: url('../../assets/img/cremaWebImg/textFooter.png');
        background-size: 100% 100%;
      }
      // .centerBottom:hover{
      //   background-image: url('../../assets/img/cremaWebImg/HovertextFooter.png');
      // }
    }
    .edges{
      background-image: url('../../assets/img/cremaWebImg/edges.png');
      background-size: 100% 100%;
      height: 580px;
      width: 100%;
      margin-top: 150px;
      .botTop{
        width: 1200px;
        height: 90px;
        line-height: 150px;
        margin: 0 auto;
        color: #fff;
        font-size: 28px;
        font-family: 'SansSerifExbFLF';
        display: flex;
        justify-content: center;
        img{
          width: 150px;
          height: 70px;
        }
      }
      .edgesAll{
        width: 1000px;
        height: 500px;
        padding: 0 0 0 40px;
        margin: 0 auto;
        // margin-top: 20px;
        display: flex;
        justify-content: space-between;
        .edgesLeft{
          width: 450px;
          height: 460px;
          padding: 100px 0 116px;
          margin: auto 0;
          .Conce{
            width: 450px;
            font-size: 20px;
            font-family: 'Montserrat-Bold';
            color: #fff;
          }
          .CLMM{
            width: 450px;
            height: 120px;
            margin-top: 40px;
            color: #959CAC;
            font-size: 18px;
            line-height: 36px;
            font-family: 'Avenir';
          }
          .edgesBtn{
            margin-top: 60px;
            width: 160px;
            // border-bottom: 1px solid rgba(#fff,.5);
            position: relative;
            display: flex;
            justify-content: space-around;
            align-items: center;
             > div:nth-child(1){
              width: 10px;
              height: 10px;
              border-radius: 50%;
              background: rgba(#959CAC,.2);
              cursor: pointer;
            }
            > div:nth-child(2){
              // position: absolute;
              top: -4px;
              left: 60px;
              width: 10px;
              height: 10px;
              border-radius: 50%;
              background: rgba(#959CAC,.2);
              cursor: pointer;
            }
            > div:nth-child(3){
              // position: absolute;
              top: -4px;
              left: 135px;
              width: 10px;
              height: 10px;
              border-radius: 50%;
              background: rgba(#959CAC,.2);
              cursor: pointer;
            }
            > div:nth-child(4){
              // position: absolute;
              top: -4px;
              left: 200px;
              width: 10px;
              height: 10px;
              border-radius: 50%;
              background: rgba(#959CAC,.2);
              cursor: pointer;
            }
            .btnSize{
              width: 60px !important;
              height: 22px !important;
              background: none !important;
              background-image: url('../../assets/img/cremaWebImg/cremaButton.png') !important;
              background-size: 100% 100% !important;
              border-radius: 0 !important;
            }
            .btnSize:hover{
              background-image: url('../../assets/img/cremaWebImg/HovercremaButton.png') !important;
            }
          }
        }
        .edgesRight{
          width: 550px;
          height: 430px;
          background-image: url('../../assets/img/cremaWebImg/edgesFlyball.png');
          background-size: 100% 100%;
        }
        .eone{
          background-image: url('../../assets/img/cremaWebImg/edgesFlyball.png');
        }
        .etwo{
          background-image: url('../../assets/img/cremaWebImg/edgesFlyballTwo.png');
        }
        .ethree{
          background-image: url('../../assets/img/cremaWebImg/edgesFlyballThree.png');
        }
        .efour{
          background-image: url('../../assets/img/cremaWebImg/edgesFlyballFour.png');
        }

      }
    }
    .Roadmap{
      position: relative;
      width: 100%;
      height: 800px;
      margin: 0 auto;
      margin-top: 30px;
      .botTop{
        width: 1200px;
        height: 150px;
        line-height: 150px;
        margin: 0 auto;
        color: #fff;
        font-size: 28px;
        font-family: 'SansSerifExbFLF';
        display: flex;
        justify-content: center;
        img{
          width: 150px;
          height: 70px;
        }
      }
      .RoadmapAll{
        width: 1000px;
        height: 650px;
        margin: 0 auto;
        background: url('../../assets/img/cremaWebImg/roadmapFive.png') no-repeat center;
        background-size: 633px 345px;
        > div:nth-child(1){
          padding-bottom: 40px;
          justify-content: space-between;
          align-items: flex-end;
          div:nth-child(1){
            width: 260px;
          }
          div:nth-child(2){
            width: 300px;
            > div{
              width: 100%;
              display: flex;
              span{
                height: 30px;
                font-size: 16px;
                color: #B6BED0;
                font-family: 'Avenir';
              }
              > div{
                width: 12px;
                height: 12px;
                margin: 6px 0 0 20px;
                background-image: url('../../assets/img/cremaWebImg/downpc.png');
                background-size: 100% 100%;
                cursor: pointer;
              }
              .jancla{
                 background-image: url('../../assets/img/cremaWebImg/uppc.png');
              }
            }
          }
          div:nth-child(3){
            width: 230px;
            > div{
              width: 100%;
              display: flex;
              span{
                height: 30px;
                font-size: 16px;
                color: #B6BED0;
                font-family: 'Avenir';
              }
              > div{
                width: 12px;
                height: 12px;
                margin: 6px 0 0 20px;
                background-image: url('../../assets/img/cremaWebImg/downpc.png');
                background-size: 100% 100%;
                cursor: pointer;
              }
              .jancla{
                 background-image: url('../../assets/img/cremaWebImg/uppc.png');
              }
            }
          }
        }
        > div:nth-child(3){
          padding-top: 40px;
          align-items: flex-start;
          justify-content: space-evenly;
          > div:nth-child(1){
            width: 355px;
            > div{
              width: 100%;
              display: flex;
              span{
                height: 30px;
                font-size: 16px;
                color: #B6BED0;
                font-family: 'Avenir';
              }
              > div{
                width: 12px;
                height: 12px;
                margin: 6px 0 0 20px;
                background-image: url('../../assets/img/cremaWebImg/downpc.png');
                background-size: 100% 100%;
                cursor: pointer;
              }
              .jancla{
                 background-image: url('../../assets/img/cremaWebImg/uppc.png');
              }
            }
          }
          > div:nth-child(2){
            width: 275px;
            > div{
              width: 100%;
              display: flex;
              span{
                height: 30px;
                font-size: 16px;
                color: #B6BED0;
                font-family: 'Avenir';
              }
              > div{
                width: 12px;
                height: 12px;
                margin: 6px 0 0 20px;
                background-image: url('../../assets/img/cremaWebImg/downpc.png');
                background-size: 100% 100%;
                cursor: pointer;
              }
              .jancla{
                 background-image: url('../../assets/img/cremaWebImg/uppc.png');
              }
            }
          }
        }
        > div:nth-child(1),
        > div:nth-child(3){
          height: 240px;
          // background: #ccc;
          display: flex;
          > div{
            padding: 20px 30px;
            background: #1F2328;
            border-radius: 10px;
            font-family: 'Avenir';
            > span{
              display: block;
              width: 100%;
              height: 30px;
              font-size: 16px;
              color: #B6BED0;
              // font-family: 'Montserrat-Bold';
            }
            > p{
              padding-left: 20px;
              color: #7A85A0;
              font-size: 14px;
              margin-bottom: 8px;
            }
          }
        }
        > div:nth-child(2){
          width: 100%;
          height: 108px;
          // display: flex;
          // flex-wrap: nowrap;
          // justify-content: center;
          > div:nth-child(1),
          > div:nth-child(3){
            height: 42px;
            width: 100%;
            display: flex;
            justify-content: space-between;
            span{
              width: 260px;
              text-align: center;
              font-size: 24px;
              line-height: 42px;
              font-family: 'Montserrat-Bold';
              color: #fff;
            }
          }
          > div:nth-child(3){
            justify-content: space-evenly;
            span{
              width: 180px;
            }
          }

          > div:nth-child(2){
            height: 24px;
            width: 1000px;
            background: url('../../assets/img/cremaWebImg/roadmapCenter.png') no-repeat center;
            background-size: 100% 100%;
          }
        }
      }
    }
    .bottom{
      // height: 970px;
      height: 845px;
      margin-top: 60px;
      background: rgba(#343F49,.1);
      // background-image: url('../../assets/img/cremaWebImg/faqbgs.png');
      // background-size: 105% 100%;
      .botTop{
        width: 1200px;
        height: 130px;
        line-height: 150px;
        margin: 0 auto;
        color: #fff;
        font-size: 28px;
        font-family: 'SansSerifExbFLF';
        display: flex;
        justify-content: center;
        img{
          width: 150px;
          height: 70px;
        }
      }
      .botBto{
        width: 800px;
        margin: 0 auto;
        > div:nth-child(1){
          font-family: 'Arial-Black';
          background: #20262A;
          width: 800px;
          height: 64px;
          margin: 0 auto;
          color: #fff;
          font-size: 16px;
          // line-height: 64px;
          margin-bottom: 2px;
          padding: 18px 30px;
          display: flex;
          justify-content: space-between;
          cursor: pointer;
          div{
            width: 12px;
            height: 12px;
            margin-top: 8px;
            background-image: url('../../assets/img/cremaWebImg/downpc.png');
            background-size: 100% 100%;
          }
          .change{
            background-image: url('../../assets/img/cremaWebImg/uppc.png');
          }
        }
        > div:nth-child(1):hover{
          background: #282F34;
        }
        > div:nth-child(2){
          font-family: 'SansSerifFLF-Demibold';
          width: 800px;
          // height: 220px;
          background: #1E2328;
          padding: 20px 30px;
          span{
            line-height: 26px;
            font-size: 18px;
            color: #959CAC;
          }
        }
      }
    }
    .bottomBig{
      height: 970px !important;
    }
  }
  .mainBig{
    height: 4860px !important;
  }
  .footer{
    height: 220px;
    width: 100%;
    background: #14191E;
    padding: 40px 0 40px 0;
    .footerAll{
      width: 1100px;
      height: 140px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      > div:nth-child(1){
        width: 100%;
        height: 26px;
        display: flex;
        flex-wrap: wrap;
        align-content: space-around;
        justify-content: space-between;
        img{
          width: 110px;
          height: 26px;
        }
        .ReiImg{
          display: flex;
          justify-content: space-between;
          align-content: space-around;
          width: 210px;
          height: 20px;
          margin-top: 3px;
          a{
            width: 20px;
            height: 20px;
            background-size: 100% 100%;
          }
          > a:nth-child(1){
          background-image: url('../../assets/img/cremaWebImg/icon_twitter@2x.png');
          }
          > a:nth-child(1):hover{
            background-image: url('../../assets/img/cremaWebImg/icon_twitter.png');
          }
          > a:nth-child(2){
            background-image: url('../../assets/img/cremaWebImg/icon_TelegramGroup@2x.png');
          }
          > a:nth-child(2):hover{
            background-image: url('../../assets/img/cremaWebImg/icon_TelegramGroup.png');
          }
          > a:nth-child(3){
            background-image: url('../../assets/img/cremaWebImg/icon_Medium@2x.png');
          }
          > a:nth-child(3):hover{
            background-image: url('../../assets/img/cremaWebImg/icon_Medium.png');
          }
          > a:nth-child(4){
            background-image: url('../../assets/img/cremaWebImg/icon_Discord@2x.png');
          }
          > a:nth-child(4):hover{
            background-image: url('../../assets/img/cremaWebImg/icon_Discord.png');
          }
        }
      }
      > div:nth-child(2){
        width: 100%;
        height: 74px;
        padding: 20px 0;
        display: flex;
        justify-content: flex-end;
        border-bottom: 1px solid rgba(#fff,.1);
        div{
          width: 155px;
          height: 40px;
          p{
            font-size: 16px;
            font-family: 'Avenir';
            text-align: right;
            color: rgba(#fff,.8);
          }
          > p:nth-child(1){
            color: rgba(255,255,255,0.5);
            font-size: 14px;
          }
        }
        > div:nth-child(1){
          margin-right: 48px;
        }
      }
      > div:nth-child(3){
        width: 100%;
        height: 16px;
        p{
          font-size: 14px;
          color: rgba(255,255,255,0.5);
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
@media screen and (max-width: 1280px) {
  .outer{
    .header{
      width: 90%;
    }
    .main{
      height: 4715px;
      .top{
        width: 1280px;
        > div:nth-child(1){
          height: 777px;
        }
        > div:nth-child(2){
          top: 490px;
        }
      }
    }
    .mainBig{
      height: 4855px !important;
    }
  }
}
@media screen and (max-width: 750px) {
  .outer {
    .header{
      width: 345px;
      height: 70px;
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
        > a{
          width: 120px;
          padding: 16px 0 0 28px;
        }
        > div{
          display: none;
        }
      }
    }
    .main{
      height: 4515px;
      .top{
        width: 100%;
        height: 370px;
         > div:nth-child(1){
          background-image: url('../../assets/img/cremaWebImg/h5HeaderBall.png');
          width: 100%;
          height: 510px;
          margin-top: -70px;
        }
        > div:nth-child(2){
            top: 290px;
          > a{
            padding: 20px 0 0 48px;
          }
        }
      }
      .center{
        height: 1390px;
        width: 100%;
        margin-top: 0;
        padding: 0 16px;
        .botTop{
          width: 100%;
          height: 32px;
          font-size: 16px;
          img{
            width: 64px;
            height: 32px;
          }
        }
        .centerAll{
          width: 330px;
          height: 390px;
          padding: 0;
          .centerTopLeft{
            width: 100%;
            height: 200px;
            padding: 245px 16px 0;
            .Conce{
              width: 100%;
              font-size: 16px;
            }
            .CLMM{
              width: 100%;
              font-size: 14px;
              line-height: 22px;
              margin-top: 16px;
            }
          }
        }
        .centerTop{
          margin-top: 100px;
          background-image: url('../../assets/img/cremaWebImg/OnehNew.png');
        }
        .centerMain{
          margin-top: 40px;
          background-image: url('../../assets/img/cremaWebImg/ThreehNew.png');
        }
        .centerBottom{
          margin-top: 40px;
          background-image: url('../../assets/img/cremaWebImg/TwohNew.png');
        }
      }
      .edges{
        margin-top: 110px;
        width: 100%;
        // width: 360px;
        margin: 110px auto 0;
        height: 536px;
        background-image: url('../../assets/img/cremaWebImg/h5edges.png');
        position: relative;
        .botTop{
          position: absolute;
          top: -120px;
          padding-left: 16px;
          width: 100%;
          height: 32px;
          font-size: 16px;
          img{
            width: 64px;
            height: 32px;
          }
        }
        .edgesAll{
          width: 100%;
          height: 100%;
          padding: 0;
          flex-wrap: wrap;
          justify-content: center;
          align-content: flex-start;
          position: relative;
          .edgesLeft{
            width: 340px;
            height: 100px;
            padding: 0 16px 0;
            margin: 20px 0 0 0;
            .Conce{
              width: 100%;
              font-size: 14px;
            }
            .CLMM{
              width: 100%;
              font-size: 14px;
              line-height: 20px;
              margin-top: 16px;
            }
            .edgesBtn{
              // display: none;
              position: absolute;
              bottom: 50px;
              left: 110px;
            }
          }
          .edgesRight{
            width: 343px;
            height: 286px;
            margin-top: 30px;
          }
        }
      }
      .Roadmap{
        background: url('../../assets/img/cremaWebImg/h5Janclab.png') no-repeat;
        background-size: 40px 1140px;
        background-position:10px 65px;
        width: 100%;
        // width: 360px;
        margin-top: 80px;
        height: 1250px;
        .botTop{
          width: 100%;
          height: 32px;
          font-size: 16px;
          line-height: 32px;
          img{
            width: 64px;
            height: 32px;
          }
        }
        .RoadmapAll{
          width: 280px;
          position: relative;
          background: none;
          > div:nth-child(1){
            height: 1000px;
            position: relative;
            >div{
              width: 300px !important;
            }
            > div:nth-child(1){
              height: 140px;
              position: absolute;
              top: 40px;
              display: flex;
              flex-wrap: wrap;
              align-content: center;
            }
            > div:nth-child(2){
              position: absolute;
              height: 200px;
              top: 500px;
              display: flex;
              flex-wrap: wrap;
              align-content: center;
              > div{
                > div{
                  display: none;
                }
              }
            }
            > div:nth-child(3){
              height: 250px;
              position: absolute;
              top: 717px;
              display: flex;
              flex-wrap: wrap;
              align-content: center;
            }
          }
          > div:nth-child(2){
            display: none;
          }
          > div:nth-child(3){
            height: 1000px;
            position: absolute;
            top: -1130px;
            display: flex;
            align-content: space-around;
            position: relative;
            > div{
              > div{
                justify-content: space-between;
              }
            }
            > div:nth-child(1){
              position: absolute;
              width: 300px;
              height: 270px;
              top: 335px;
              display: flex;
              flex-wrap: wrap;
              align-content: center;
              > div:nth-child(2){
                margin-bottom: 20px;
              }
            }
            > div:nth-child(2){
              position: absolute;
              height: 220px;
              width: 300px;
              top: 1115px;
              display: flex;
              flex-wrap: wrap;
              align-content: center;
            }
          }
          > div:nth-child(1),
          > div:nth-child(3){
            width: 300px;
            flex-wrap: wrap;
            > div{
              padding: 10px 20px;
              > div{
                > div{
                  display: none;
                }
              }
            }
          }
        }
        // > div:nth-child(3){
        //   position: absolute;
        //   top: 0;
        //   left: 10px;
        //   width: 28px;
        //   height: 200px;
        //   background-image: url('../../assets/img/cremaWebImg/h5linecA.png');
        //   background-size: 100% 100%;
        // }
      }
      .bottom{
        height: 738px;
        width: 100%;
        padding-top: 1px;
        .botTop{
          margin: 30px 0;
          width: 100%;
          height: 32px;
          font-size: 16px;
          line-height: 32px;
          img{
            width: 64px;
            height: 32px;
          }
        }
        .botBto{
          // display: none;
          width: 80%;
          > div:nth-child(1){
            padding: 14px 20px;
            width: 100%;
            // line-height: 30px;
            font-size: 12px;
            height: 60px;
            span{
              width: 210px;
            }
            .cftcy{
              margin-top: 6px;
            }
          }
          > div:nth-child(2){
            // height: 220px;
            width: 100%;
            padding: 5px 20px;
            span{
              font-size: 12px;
              line-height: 15px;
            }
          }
        }
        
      }
      .bottomBig{
        height: 955px !important;
      }
    }
    .mainBig{
      height: 4750px !important;
    }
    .footer{
      width: 100%;
      height: 220px;
      padding: 0 0 0 0;
      background-image: url('../../assets/img/cremaWebImg/footerbgs.png');
      background-size: 100% 100%;
      .footerAll{
        width: 100%;
        height: 200px;
        > div:nth-child(1){
          justify-content: center;
          margin: 0 auto;
          height: 100px;
          width: 60%;
        }
        > div:nth-child(2){
          height: 52px;
          padding: 0 10px;
          justify-content: space-between;
          > div:nth-child(1){
            margin-right: 0;
          }
          div{
            width: 180px;
             p{
              text-align: center;
            }
          }
        }
        > div:nth-child(3){
          // display: none;
          p{
            text-align: center;
          }
        }
        .footerLeft{
          margin: 0 auto;
          height: 210px;
          img{
            margin: -46px auto 0;
          }
          p{
            margin: 20px auto -30px;
          }
        }
        .footerReight{
          width: 100%;
          position: absolute;
          height: 66px;
          // left: 106px;
          top: 65px;
          margin: 0 auto;
          justify-content: center;
          .ReiImg{
            width: 240px;
            margin-top: -6px;
          }
          p{
            margin: 12px auto 0;
          }
          .oneEmail{
            margin: 0;
            margin-top: 22px;
          }
        }
      }
    }
  }
}
</style>
