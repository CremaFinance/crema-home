<template>
  <div class="outer">
    <!-- 头部导航栏区域 -->
    <div class="headerAll">
      <div class="header">
        <div class="navLeft">
          <img src="../../assets/img/cremaWebImg/headerLogo.png">
        </div>
        <div class="navReight">
          <div>
            <a href="https://twitter.com/Crema_Finance" target="_blank"></a>
            <a href="https://t.me/cremafinance" target="_blank"></a>
            <a href="https://medium.com/@Crema.finance" target="_blank"></a>
            <a href="https://discord.gg/hCaFmvvPYH" target="_blank"></a>
          </div>
          <div class="center"></div>
          <a href="https://app.crema.finance/#/" target="_blank">Launch APP</a>
        </div>
      </div>
    </div>
    <!-- 主体区域 -->
    <div class="main" :class="faqVal ? 'mainBig':''">
      <div class="top">
          <div>
            <div class="headerTop">
              <div></div>
            </div>
            <div class="topText">
              <p>A Powerful Concentrated Liquidity Protocol</p>
              <div>Swap, earn and build with Crema's programmable liquidity network and unleash the full potential of your assets.</div>
            </div>
            <div class="boootmB">
              <a href="https://app.crema.finance/#/" target="_blank"><span>Launch APP</span></a>
              <a href="https://gitbook.crema.finance/" target="_blank"><span>Docs</span></a>
            </div>
          </div>
          <div>
            <video class="webMp" muted playsinline loop autoplay data-wf-ignore="true" data-object-fit="cover">
              <source src="../../assets/img/cremaWebImg/covercc.webm" type="video/mp4">
            </video>
            <video class="hfiveMp" preload="none" muted playsinline loop autoplay data-wf-ignore="true" data-object-fit="cover">
              <source src="../../assets/img/cremaWebImg/cremanewH5.webm" type="video/mp4">
            </video>
          </div>
      </div>
      <div class="products"  :class="productsDetail ? 'productsNew':''">
        <div>
          <div class="botTop">
            <span>Our Products</span>
          </div>
          <div class="botCenter" :class="productsDetail ? 'fivenew':''">
            <p @click="changeP('a')" :class="changeVal == 'a'? 'changeClass':''">Concentrated Liquidity</p>
            <p @click="changeP('b')" :class="changeVal == 'b'? 'changeClass':''">NFT Liquidity Farming</p>
            <p @click="changeP('c')" :class="changeVal == 'c'? 'changeClass':''">Smart Router</p>
            <p @click="changeP('d')" :class="changeVal == 'd'? 'changeClass':''">Cross-Chain Solutions</p>
            <div>
                <span @click="changehFive()" :class="changeVal == 'a' ? 'changepas' : ''">Concentrated Liquidity</span>
                <span @click="changeP('b')" v-if="productsDetail"  :class="changeVal == 'b' ? 'changepas' : ''">NFT Liquidity Farming</span>
                <span @click="changeP('c')" v-if="productsDetail"  :class="changeVal == 'c' ? 'changepas' : ''">Smart Router</span>
                <span @click="changeP('d')" v-if="productsDetail"  :class="changeVal == 'd' ? 'changepas' : ''">Cross-Chain Solutions</span>
                <div @click="changehFive()" :class="productsDetail ? 'changeFive' : ''"></div>
            </div>
          </div>
          <div>
            <div>
              <p>{{ changeValDetail.top }}</p>
              <p>{{ changeValDetail.bottom }}</p>
            </div>
            <div :class="changeVal == 'a'? 'classA' : changeVal == 'b'? 'classB' : changeVal == 'c'? 'classC' : 'classD'"></div>
          </div>
        </div>
        <div></div>
        <div></div>
      </div>
      <div class="center">
        <div class="botTop">
          <span>Our Edges</span>
          <!-- <img src="../../assets/img/cremaWebImg/cremaTitlea.png" alt=""> -->
        </div>
        <div class="centerTop centerAll">
          <div class="centerTopLeft">
            <p>For Traders</p>
            <div class="Conce">Embrace the higher market depth and lower price slippage</div>
            <div class="CLMM">The price impact of user orders is much less on CLMM pools because there is more liquidity concentrated around the current price.</div>
          </div>
          <div></div>
        </div>
        <div class="centerMain centerAll">
          <div class="centerTopLeft">
            <p>For Liquidity Providers</p>
            <div class="Conce">Maximize the utilization of their capital </div>
            <div class="CLMM">LPs can earn transaction fees more efficiently by specifying a narrow and reasonable price range. Extra incentives will also be distributed through NFT liquidity farming.</div>
          </div>
          <div></div>
        </div>
        <div class="centerBottom centerAll">
          <div class="centerTopLeft">
            <p>For Developers</p>
            <div class="Conce">Integrate Crema's service with no barriers</div>
            <div class="CLMM">Crema will be a core building block of the Defi 2.0 infrastructure on Solana. Any Solana-based application can easily call or integrate Crema's service with its ready-to-use SDK.</div>
          </div>
          <div></div>
        </div>
      </div>
      <div class="Roadmap">
        <div class="botTop">
          <span>Roadmap</span>
        </div>
         <div class="RoadmapAll">
           <div>
             <div>
               <span>Project Started</span>
               <span>R&D Started</span>
               <span>Devnet Beta Release</span>
             </div>
             <div>
               <span>TGE & IDO</span>
               <div>
                  <span>V1.0 Release</span>
                  <div @click="changeJan" :class="isJan ? 'jancla':''"></div>
               </div>
               <div v-show="isJan"><p v-for="(item,index) in janForm" :key="index">{{item.val}}</p></div>
               <span>Multichain Versions</span>
             </div>
             <div>
                <div>
                  <span>DAO Platform Started</span>
                  <div @click="changemar" :class="ismar ? 'jancla':''"></div>
                </div>
                <div v-show="ismar"><p v-for="(item,index) in marForm" :key="index">{{item.val}}</p></div>
                <div>
                </div>
                <span>Internal Oracle</span>
             </div>
           </div>
           <div>
             <div>
               <span>2021 Nov</span>
               <span>2022 Q1</span>
               <span>2022 Q3</span>
             </div>
             <div></div>
             <div>
               <span>2021 Dec</span>
               <span>2022 Q2</span>
             </div>
           </div>
           <div>
             <div>
               <div>
                  <span>Mainnet Beta Release</span>
                  <div @click="changedec" :class="isdec ? 'jancla':''"></div>
               </div>
               <div v-show="isdec"><p v-for="(item,index) in decForm" :key="index">{{item.val}}</p></div>
               <div>
                  <span>Integrate with Aggregators</span>
                  <div @click="changeint" :class="isint ? 'jancla':''"></div>
               </div>
               <div v-if="isint"><p v-for="(item,index) in intForm" :key="index">{{item.val}}</p></div>
             </div>
             <div>
              <span>Cross-Chain Swap</span>
              <span>Liquidity Migration</span>
              <span>CLMM V2</span>
             </div>
           </div>
        </div>
        <div class="RoadmapAllH">
          <div>
            <div>
              <div></div>
              <div></div>
            </div>
            <div>
              <div>2021 Nov</div>
              <div>
                <p>Project Started</p>
                <p>R&D Started</p>
                <p>Devnet Beta Release</p>
              </div>
            </div>
          </div>
          <div>
            <div>
              <div></div>
              <div></div>
            </div>
            <div>
              <div>2021 Dec</div>
              <div>
                <div>
                  <p>Mainnet Beta Release</p>
                  <div @click="changedec" :class="isdec ? 'jancla':''"></div>
                </div>
                <div class="changeRoad" v-if="isdec"><span v-for="(item,index) in decForm" :key="index">{{item.val}}</span></div>
                <div>
                    <p>Integrate with Aggregators</p>
                    <div @click="changeint" :class="isint ? 'jancla':''"></div>
                </div>
                <div class="changeRoad" v-if="isint"><span v-for="(item,index) in intForm" :key="index">{{item.val}}</span></div>
              </div>
            </div>
          </div>
          <div>
            <div>
              <div></div>
              <div></div>
            </div>
            <div>
              <div>2022 Q1</div>
              <div>
                <p>TGE & IDO</p>
                <div>
                    <p>V1.0 Release</p>
                    <div @click="changeJan" :class="isJan ? 'jancla':''"></div>
                </div>
                <div class="changeRoad" v-if="isJan"><span v-for="(item,index) in janForm" :key="index">{{item.val}}</span></div>
                <p>Multichain Versions</p>
              </div>
            </div>
          </div>
          <div>
            <div>
              <div></div>
              <div></div>
            </div>
            <div>
              <div>2022 Q2</div>
              <div>
                <p>Cross-Chain Swap</p>
                <p>Liquidity Migration</p>
                <p>CLMM V2</p>
              </div>
            </div>
          </div>
          <div>
            <div>
              <div></div>
              <div></div>
            </div>
            <div>
              <div>2022 Q3</div>
              <div>
                <div>
                    <p>DAO Platform Started</p>
                    <div @click="changemar" :class="ismar ? 'jancla':''"></div>
                </div>
                <div class="changeRoad" v-if="ismar"><span v-for="(item,index) in marForm" :key="index">{{item.val}}</span></div>
                <p>Internal Oracle</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="bottom" :class="faqVal ? 'bottomBig':''">
        <div class="botTop">
          <span>FAQ</span>
        </div>
        <div class="botBto" v-for="(item,index) in faqForm" :key="index"  @click="faqText(item)">
          <div>
            <span :class="item.ccp ? 'cftcy':''">{{item.value}}</span>
            <div :class="faqVal == item.child ? 'change' : ''"></div>
          </div>
          <div v-if="faqVal == item.child">
            <span>{{item.child}}</span>
          </div>
        </div>
      </div>
      <div class="footerBot"></div>
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
            <p>Business Cooperation</p>
            <p>bd@crema.finance</p>
          </div>
          <div>
            <p>General Inquiries</p>
            <p>hello@crema.finance</p>
          </div>
        </div>
        <div>
            <p>© 2022 Crema. All rights reserved.</p>
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
          val:'Info Charts'
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
          val:'veCRM Stake and Mint'
        },
        {
          val:'Proposal and Voting'
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
      // locale: "简体中文",
      timer: '',
      value: 0,
      // 监视数据
      changeVal:'',
      changeValDetail:{
        top:'',
        bottom:'',
      },
      productsDetail:false,
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
  mounted() {this.changeP('a');},
  methods: {
    changehFive(){
      this.faqVal = '';
      this.productsDetail = !this.productsDetail;
      this.changeP('a');
    },
    changeP(val){
      this.changeVal = val;
      // this.productsDetail = false;
      if(val=='a'){
        this.changeValDetail.top = 'Concentrated Liquidity Market Maker',
        this.changeValDetail.bottom = 'CLMM allows liquidity providers to set specific price ranges, add single-sided liquidity and do range order trading. It redefines the capital efficiency and trading depth on Solana.'
      }
      if(val=='b'){
        this.changeValDetail.top = 'NFT Liquidity Farming',
        this.changeValDetail.bottom = "A special gift from Crema. The non-fungible liquidity contributed by liquidity providers are eligible to earn extra rewards from Crema's NFT Liquidity Farming pools."
      }
      if(val=='c'){
        this.changeValDetail.top = 'Smart Router',
        this.changeValDetail.bottom = "Externally integrated by Jupiter, the powerful aggregator on Solana, internally equipped with Crema's own routing system, Crema always delivers the best price in the ecosystem to its users. "
      }
      if(val=='d'){
        this.changeValDetail.top = 'Cross-Chain Solutions',
        this.changeValDetail.bottom = "Powered by CLMM pools and the internal routing system, Crema can be a liquidity bridge for any cross-chain platforms. With dedicated smart contracts deployed on multiple blockchains, cross-chain swap has never been easier."
      }

    },
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
    faqText(e){
      this.productsDetail = false;
      if(this.faqVal && this.faqVal == e.child){
        this.faqVal = '';
        return;
      }
      this.faqVal = e.child;
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
  watch:{}
};
</script>
<style lang="scss" scoped>
.outer {
  width: 100%;
  height: 100%;
  background: #13191f;
  position: relative;
  font-family: 'Helvetica-NeueBd';
  .headerAll{
    width: 100%;
    background: #000;
    .header {
      width: 1000px;
      height: 80px;
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
          width: 160px;
          height: 36px;
        }
      }
      .navReight{
        height: 46px;
        width: 370px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        > a{
          display: block;
          width: 138px;
          height: 46px;
          background-image: url('../../assets/img/cremaWebImg/buttonHeadca.png');
          background-size: 100% 100%;
          cursor: pointer;
          font-size: 12px;
          padding: 15px 32px;
          color: #fff;
          font-family: 'Helvetica-NeueBd';
        }
        > a:hover{
          background-image: url('../../assets/img/cremaWebImg/HoverbuttonHeadc.png');
        }
        .center{
          width: 1px;
          height: 24px;
          border-right: 1px solid #808080;
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
  }
  .main{
    width: 100%;
    position: relative;
    // overflow: hidden;
    object-fit: cover;
    .top{
      height: 580px;
      width: 100%;
      display: flex;
      justify-content: center;
      margin: 0 auto;
      position: relative;
      flex-wrap: wrap;
      > div:nth-child(1){
        width: 1000px;
        height: 600px;
        margin: 0 auto;
        position: relative;
        z-index: 20;
        display: flex;
        flex-wrap: wrap;
        align-content: center;
        .headerTop{
          height: 36px;
          > div{
            width: 206px;
            height: 36px;
            background-image: url('../../assets/img/cremaWebImg/changecvr.png');
            background-size: 100% 100%;
          }
        }
        .topText{
          width: 100%;
          height: 210px;
          padding: 20px 0 20px 0;
          color:#fff;
          display: flex;
          flex-wrap: wrap;
          font-family: 'Helvetica-NeueBd';
          align-content: space-between;
          p{
            width: 500px;
            font-size: 36px;
            line-height: 48px;
          }
          div{
            font-size: 18px;
            width: 55%;
            line-height: 30px;
            color: #ddd;
            font-family: 'Helvetica-NeueBd';
          }
        }
        .boootmB{
          height: 90px;
          display: flex;
          margin-top: 30px;
          > a{
            display: block;
            font-family: 'Helvetica-NeueBd';
            background-size: 100% 100%;
            font-size: 20px;
            color: #fff;
            padding: 8px 0;
            display: flex;
            justify-content: center;
            width: 165px;
            height: 42px;
          }
          > a:nth-child(1){
            background-image: url('../../assets/img/cremaWebImg/buttonHeadf.png');
          }
          > a:nth-child(1):hover{
            background-image: url('../../assets/img/cremaWebImg/buttonHeadg.png');
          }
          > a:nth-child(2){
            margin-left: 20px;
            background-image: url('../../assets/img/cremaWebImg/webimgs.png');
          }
          > a:nth-child(2):hover{
            background-image: url('../../assets/img/cremaWebImg/webhover.png');
          }
        }
      }
      > div:nth-child(2){
        width: 100%;
        position: absolute;
        background: #000;
        height: 560px;
        // video{
        //   margin: auto;
        //   min-width: 100%;
        //   min-height: 100%;
        //   height: auto;
        //   width: auto;
        //   z-index: 2;
        // }
        video{
          position: absolute;
          left: 23%;
          top: 30px;
          width: 70%;
          height: 480px;
          z-index: 2;
        }
        .hfiveMp{
          display: none;
        }
      }
    }
    .products{
      width: 100%;
      height: 650px;
      margin-top: 30px;
      color: #fff;
      position: relative;
      > div:nth-child(1){
        width: 1000px;
        height: 100%;
        margin: 0 auto;
        .botTop{
          height: 90px;
          line-height: 55px;
          margin: 0 auto;
          color: #fff;
          font-size: 32px;
          display: flex;
          justify-content: center;
          font-family: 'Helvetica-NeueBd';
        }
        .botCenter{
          width: 100%;
          height: 80px;
          background: rgba(#fff,.1);
          border-radius: 40px;
          display: flex;
          justify-content: space-around;
          align-items: center;
          position: relative;
          z-index: 20;
          p{
            font-size: 14px;
            color: rgba(#fff,.7);
            padding: 0 15px;
            height: 40px;
            text-align: center;
            line-height: 40px;
            cursor: pointer;
            font-family: 'Helvetica-Black';
          }
          .changeClass{
            background: linear-gradient(270deg, #5FE6D0 0%, #60B2F1 33%, #9380FF 68%, #E590FF 100%);
            border-radius: 20px;
            color: #fff !important;
          }
          > div{
            display: none;
          }
        }
        > div:nth-child(3){
          margin-top: 60px;
          width: 100%;
          height: 380px;
          display: flex;
          justify-content: space-between;
          > div:nth-child(1){
            width: 480px;
            height: 100%;
            display: flex;
            flex-wrap: wrap;
            padding: 110px 0;
            p{
              font-size: 24px;
              line-height: 28px;
            }
            > p:nth-child(2){
              font-size: 16px;
              font-family: 'Helvetica-NeueLt';
              color: rgba(#fff,.7);
            }
          }
          > div:nth-child(2){
            width: 450px;
            height: 100%;
            background-size: 100% 100%;
          }
          .classA{
            background-image: url('../../assets/img/cremaWebImg/edgesFlyball.png');
          }
          .classB{
            background-image: url('../../assets/img/cremaWebImg/edgesFlyballThree.png');
          }
          .classC{
            background-image: url('../../assets/img/cremaWebImg/edgesFlyballTwo.png');
          }
          .classD{
            background-image: url('../../assets/img/cremaWebImg/edgesFlyballFouryna.png');
          }
        }
      }
      > div:nth-child(2),
      > div:nth-child(3){
        position: absolute;
        width: 475px;
        height: 100%;
        background-size: 100% 100%;
        top: 0;
      }
      > div:nth-child(2){
        background-image: url('../../assets/img/cremaWebImg/productsLeft.png');
        left: 0;
      }
      > div:nth-child(3){
        background-image: url('../../assets/img/cremaWebImg/productsRight.png');
        right: 0;
      }
    }
    .center{
      height: 1450px;
      width: 100%;
      .botTop{
        width: 1000px;
        height: 150px;
        line-height: 150px;
        margin: 0 auto;
        color: #fff;
        font-size: 32px;
        font-family: 'Helvetica-NeueBd';
        display: flex;
        justify-content: center;
        img{
          width: 150px;
          height: 70px;
        }
      }
      .centerAll{
        width: 1000px;
        height: 380px;
        padding: 0 0 0 80px;
        margin: 0 auto;
        border-radius: 30px;
        display: flex;
        justify-content: space-between;
        background: #1F2328;
        border-radius: 20px;
        .centerTopLeft{
          width: 370px;
          height: 380px;
          padding: 55px 0;
          margin: auto 0;
          p{
            height: 36px;
            font-style: 16px;
            font-family: 'Arial';
            margin-bottom: 20px;
            text-align: center;
            border-radius: 18px;
            line-height: 36px;
          }
          .Conce{
            font-size: 24px;
            line-height: 30px;
            color: #fff;
          }
          .CLMM{
            width: 322px;
            margin-top: 40px;
            color: rgba(#fff,.7);
            font-size: 16px;
            line-height: 28px;
            font-family: 'Helvetica-NeueLt';
          }
        }
        > div:nth-child(2){
          width: 480px;
          height: 100%;
          background-size: 100% 100%;
        }
      }
      .centerTop{
        > div:nth-child(2){
          background-image: url('../../assets/img/cremaWebImg/usdcFirst.png');
        }
        .centerTopLeft{
          p{
            color: #9EAAF7;
            background: #1B2775;
            width: 130px;
          }
        }
      }
      .centerMain{
        margin-top: 30px;
        > div:nth-child(2){
          background-image: url('../../assets/img/cremaWebImg/usdcTwo.png');
        }
        .centerTopLeft{
           p{
            color: #9EDFF7;
            background: #224F63;
            width: 200px;
          }
        }
      }
      .centerBottom{
        margin-top: 30px;
        > div:nth-child(2){
          background-image: url('../../assets/img/cremaWebImg/usdcThree.png');
        }
        .centerTopLeft{
          p{
            color: #C49EF7;
            background: #3A2273;
            width: 150px;
          }
        }
      }
    }
    .Roadmap{
      position: relative;
      width: 100%;
      height: 700px;
      margin: 0 auto;
      .botTop{
        width: 900px;
        height: 100px;
        line-height: 70px;
        margin: 0 auto;
        color: #fff;
        font-size: 32px;
        font-family: 'Helvetica-NeueBd';
        display: flex;
        justify-content: center;
      }
      .RoadmapAll{
        width: 1000px;
        height: 650px;
        margin: 0 auto;
        background: url('../../assets/img/cremaWebImg/roadmapFive.png') no-repeat center;
        background-size: 633px 345px;
        > div:nth-child(1){
          height: 210px !important;
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
                font-family: 'Helvetica-NeueLt';
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
            > div:nth-child(3){
              display: block;
            }
          }
          div:nth-child(3){
            width: 250px;
            > div{
              width: 100%;
              display: flex;
              span{
                height: 30px;
                font-size: 16px;
                color: #B6BED0;
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
            > div:nth-child(2){
              display: block;
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
            > div:nth-child(2){
              display: block;
            }
            > div:nth-child(4){
              display: block;
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
          display: flex;
          > div{
            padding: 20px 30px;
            background: #1F2328;
            border-radius: 10px;
            font-family: 'Helvetica-NeueLt';
            > span{
              display: block;
              width: 100%;
              height: 30px;
              font-size: 16px;
              color: #B6BED0;
            }
            p{
              padding-left: 20px;
              color: #7A85A0;
              font-size: 14px;
              margin-bottom: 12px;
              font-family: 'Helvetica-NeueLt';
            }
          }
        }
        > div:nth-child(2){
          width: 100%;
          height: 108px;
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
      .RoadmapAllH{
        display: none;
      }
    }
    .bottom{
      height: 845px;
      position: relative;
      z-index: 20;
      .botTop{
        width: 900px;
        height: 100px;
        line-height: 70px;
        margin: 0 auto;
        color: #fff;
        font-size: 32px;
        font-family: 'Helvetica-NeueBd';
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
          font-family: 'Helvetica-NeueBd';
          background: #20262A;
          width: 800px;
          height: 64px;
          margin: 0 auto;
          color: #fff;
          font-size: 16px;
          margin-bottom: 10px;
          padding: 22px 30px;
          display: flex;
          justify-content: space-between;
          cursor: pointer;
          div{
            width: 12px;
            height: 12px;
            margin-top: 6px;
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
          font-family: 'Helvetica-NeueLt';
          width: 800px;
          background: #1E2328;
          padding: 20px 30px;
          span{
            line-height: 26px;
            font-size: 16px;
            color: #959CAC;
          }
        }
      }
    }
    .bottomBig{
      height: 1080px !important;
      .botBto{
        > div:nth-child(1){
          margin-bottom: 10px;
        }
        > div:nth-child(2){
          margin-bottom: 10px;
        }
      }
    }
    .footerBot{
      position: absolute;
      width: 100%;
      height: 200px;
      z-index: 1;
      left: 0;
      bottom: 0;
      background-image: url('../../assets/img/cremaWebImg/bottomSi.png');
      background-size: 100% 100%;
    }
  }
  .mainBig{
    height: 4600px !important;
  }
  .footer{
    height: 220px;
    width: 100%;
    background: #14191E;
    padding: 40px 0 40px 0;
    .footerAll{
      width: 1000px;
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
  25% { transform: translateY(-4px);}
  50%,
  100% { transform: translateY(0);}
  75% { transform: translateY(4px);}
}
@keyframes bounce-opcity {
  25% {}
  // 40%{}
  50% {}
  75% {}
  // 75% {}
  100% {}
}
@media screen and (max-width: 1280px) {
  .outer{
    .main{
      .bottom{
        height: 945px;
      }
      .bottomBig{
        height: 1085px !important;
      }
    }
    .mainBig{
      height: 4555px !important;
    }
  }
}
@media screen and (max-width: 1015px) {
  .outer{
    .headerAll{
      width: 1000px;
    }
    .main{
      .bottom{
        height: 945px;
      }
      .bottomBig{
        height: 1085px !important;
      }
      .top{
        width: 1000px;
      }
      .products{
        width: 1000px;
      }
    }
    .mainBig{
      height: 4555px !important;
    }
  }
}
@media screen and (max-width: 750px) {
  .outer {
    background: #13191f;
    .headerAll{
      width: 100%;
      .header{
        width: 85%;
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
            padding: 14px 0 0 22px;
          }
          > div{
            display: none;
          }
        }
      }
    }
    .main{
      .top{
        width: 100%;
        height: 550px;
        background: #000;
        overflow: hidden;
        > div:nth-child(1){
          width: 100%;
          height: 100%;
          position: relative;
          .headerTop{
            width: 100%;
            position: absolute;
            top: 40px;
            left: 0;
            height: 48px;
            padding-left: 0;
            > div{
              margin: 0 auto;
            }
          }
          .topText{
            position: absolute;
            top: 80px;
            height: 225px;
            padding: 0 0 0 0;
            text-align: center;
            justify-content: center;
            align-content: space-around;
            p{
              font-size: 28px;
              width: 70%;
              line-height: 35px;
            }
            div{
              font-size: 14px;
              width: 95%;
              line-height: 24px;
              padding: 0 25px;
            }
          }
          .boootmB{
            width: 100%;
            justify-content: space-around;
            position: absolute;
            bottom: -20px;
            padding: 0 30px;
            > a{
              padding: 8px 0;
              width: 132px !important;
              height: 40px !important;
            }
          }
        }
        > div:nth-child(2){
          height: 560px;
          video{
            position: absolute;
            left: 0;
            top: 92px;
            width: 100%;
            height: 650px;
            z-index: 2;
            /* background: transparent url('../../assets/img/cremaWebImg/hFicrema.png') 100% 100% / cover no-repeat ; */
            background: url('../../assets/img/cremaWebImg/hFicrema.png') center center no-repeat;
            background-size: 100% auto;
          }
          .webMp{
            display: none;
          }
          .hfiveMp{
            display: block;
          }
        }
      }
      .products{
        margin-top: 20px;
        width: 100%;
        height: 700px;
        color: #fff;
        position: relative;
        > div:nth-child(1){
          width: 100%;
          height: 100%;
          margin: 0 auto;
          .botTop{
            width: 100%;
            height: 64px;
            font-size: 16px;
            line-height: 64px;
          }
          .botCenter{
            margin: 0 auto;
            width: 336px;
            height: 52px;
            p{
              display: none;
            }
            > div{
              display: block;
              width: 300px;
              height: 32px;
              color: #fff !important;
              position: relative;
              .changepas{
                background: linear-gradient(270deg, #5FE6D0 0%, #60B2F1 33%, #9380FF 68%, #E590FF 100%);
                border-radius: 20px;
              }
              span{
                display: block;
                width: 100%;
                height: 100%;
                line-height: 32px;
                text-align: center;
              }
              div{
                position: absolute;
                width: 16px;
                height: 16px;
                right: 16px;
                top: 8px;
                background-image: url('../../assets/img/cremaWebImg/arrowDown.png');
                background-size: 100% 100%;
              }
              .changeFive{
                background-image: url('../../assets/img/cremaWebImg/arrowUp.png');
              }
            }
          }
          .fivenew{
            height: 200px;
            align-items: flex-start;
            padding-top: 10px;
            border-radius: 20px;
            >div{
              >span:nth-of-type(n+2){
                height: 32px;
                line-height: 32px;
                margin-top: 16px;
              }
            }
          }
          > div:nth-child(3){
            margin-top: 30px;
            height: 550px;
            justify-content: center;
            align-content: space-around;
            align-items: center;
            flex-wrap: wrap;
            > div:nth-child(1){
              width: 345px;
              height: 180px;
              padding: 0 0 0 15px;
              > p:nth-child(2){
                margin-top: 20px;
              }
            }
            > div:nth-child(2){
              width: 345px;
              height: 286px;
            }
          }
        }
        > div:nth-child(2){
          width: 100%;
        }
        > div:nth-child(3){
          display: none;
        }
      }
      .productsNew{
        height: 830px;
      }
      .center{
        height: 1800px;
        width: 100%;
        margin-top: 0;
        .botTop{
          width: 100%;
          height: 32px;
          font-size: 16px;
          line-height: 30px;
        }
        .centerAll{
          width: 340px;
          height: 535px;
          padding: 0;
          flex-wrap: wrap;
          align-content: space-between;
          border-radius: 10px;
          .centerTopLeft{
            height: 230px;
            padding: 20px 15px 0;
            .Conce{
              font-size: 16px;
            }
            .CLMM{
              width: 100%;
              font-size: 14px;
              line-height: 22px;
              margin-top: 16px;
            }
          }
          > div:nth-child(2){
            width: 100%;
            height: 270px;
          }
        }
        .centerTop{
          margin-top: 30px;
        }
        .centerMain{
          margin-top: 40px;
        }
        .centerBottom{
          margin-top: 40px;
        }
      }
      .Roadmap{
        // background: url('../../assets/img/cremaWebImg/h5Janclab.png') no-repeat;
        background-size: 40px 1140px;
        background-position:10px 65px;
        width: 100%;
        height: 100%;
        .botTop{
          width: 100%;
          height: 32px;
          font-size: 16px;
          line-height: 32px;
        }
        .RoadmapAll{
          display: none;
        }
        .RoadmapAllH{
          display: block;
          width: 300px;
          margin: 34px auto 0;
          height: 100%;
          color: #fff;
          > div{
            display: flex;
            justify-content: space-between;
            > div:nth-child(1){
              width: 20px;
              > div:nth-child(1){
                width: 20px;
                height: 20px;
                background: url('../../assets/img/cremaWebImg/spanceBut.png') no-repeat;
                background-size: 100% 100%;
              }
              > div:nth-child(2){
                width: 0px;
                height: 90%;
                margin: 0 auto;
                border-right: 2px solid;
                border-image: linear-gradient(360deg, rgba(171, 108, 255, 0), rgba(125, 255, 238, 1)) 2 2;
              }
            }
            > div:nth-child(2){
              width: 260px;
              > div:nth-child(1){
                font-size: 20px;
              }
              > div:nth-child(2){
                width: 100%;
                background: #1F2328;
                border-radius: 10px;
                padding: 30px 15px;
                margin-top: 10px;
                span{
                  display: block;
                  font-size: 12px;
                  color: #7A85A0;
                  line-height: 20px;
                  margin-left: 10px;
                  font-family: 'Helvetica-NeueLt';
                }
                p{
                  line-height: 30px;
                  font-size: 14px;
                  font-family: 'Helvetica-NeueLt';
                  color: #B6BED0;
                }
                > div{
                  display: flex;
                  > div{
                    width: 12px;
                    height: 12px;
                    margin: 10px 0 0 20px;
                    background-image: url('../../assets/img/cremaWebImg/downpc.png');
                    background-size: 100% 100%;
                  }
                  .jancla{
                    background-image: url('../../assets/img/cremaWebImg/uppc.png');
                  }
                }
              }
              .changeRoad{
                display: block !important;
              }
            }
          }
          > div:nth-child(2),
          > div:nth-child(3),
          > div:nth-child(4),
          > div:nth-child(5){
            margin-top: 20px;
          }
        }
      }
      .bottom{
        height: 800px;
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
          width: 80%;
          > div:nth-child(1){
            padding: 14px 20px;
            width: 100%;
            font-size: 14px;
            height: 60px;
            span{
              width: 210px;
              line-height: 16px;
            }
            .cftcy{
              margin-top: 6px;
            }
          }
          > div:nth-child(2){
            width: 100%;
            padding: 5px 20px;
            span{
              font-size: 12px;
              line-height: 18px;
            }
          }
        }

      }
      .bottomBig{
        height: 1055px !important;
      }
      .footerBot{
        height: 70px;
      }
    }
    .mainBig{
      height: 100% !important;
    }
    .footer{
      width: 100%;
      height: 240px;
      padding: 20px 0 0 0;
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
          .ReiImg{
            width: 80%;
          }
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
              font-size: 14px;
            }
          }
        }
        > div:nth-child(3){
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
