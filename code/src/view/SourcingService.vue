<template>
  <div id="CompanyIntroduction">
    <div class="banner container-fuild text-center"></div>
    <div class="container">
      <div class="row CompanyIntroduction-container" v-for="item in list" :key="item.title">
        <div class="col-xs-10 col-sm-10 col-md-5 wow zoomIn">
          <img class="img-responsive center-block" :src="item.img" />
        </div>
        <div @click="clickBlog" class="col-xs-14 col-sm-14 col-md-7">
          <h3 style="fontWeight:bold">{{item.title}}</h3>
          <p class=".text-justify" v-for="p in item.content" :key="p">{{p}}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from "wowjs";
export default {
  name: "CompanyIntroduction",
  data() {
    return {
      list: [
        {
          title: "How do we source in China ?",
          content: [
            "Step 1:  Just send us product link (ebay,amazon,shopify,dhgate,aliexpress,etc) or image.You can also make an excel file to us if you are looking for many different products in one time,this is more efficient.",
            "Step 2: We will contact over 15 suppliers in China, and send you our best wholesale price within 1 working day.",
            "Step 3: If you need check quality,we can arrange free sample before order confirmed. ",
            "Step 4: You make payment according to price, quantity and postage (Payment accept T/T,Western Union,Paypal,Moneygram,etc.)",
            "Step 5: We order products from suppliers within 24 hours after payment received.",
            "Step 6: Only 1-3 days, we can receive your products from different suppliers, we will check and take product photos to you to double confirm, them repack products according to your requirement.",
            "Step 7:  After getting your approval,we will send your parcels to you via air/sea/train/truck, we offer door to door service and tax free. Drop shipping is also available.",
            "Step 8: You will receive your parcel by DHL/FEDEX/TNT/UPS,or by sea, by train,by truck,etc. We will track your parcel after you received."
          ],
          img:require('@/assets/img/sourcing_1.jpg')
        },
        {
          title: "Why choose us ?",
          content: [
            "Our main customers are like you who running online shop on ebay,Amazon,shopify,or on their own company website. ",
            "They have imported from China many years via Aliexpress,Dhgate,etc,but now they work with us,why ?",
            "1. Aliexpress is retail price,we can do lower wholesale price. Just send us product link or image,we can quote within 24 hours.",
            "2. We can do better freight, help you save freight and time.",
            "When you order different products from different Chinese suppliers,you have to pay international freight many times.It increase your shipping cost, waste your time to track different parcels, and parcels are easily lost due to long shipping time.",
            "We can help you order them and ship from our warehouse,cost lower freight and more efficient delivery.",
            "3. You run many online shops, want to expand business ?",
            "When you run many online shops,you spend a lot time on shop and marketing,you don't want contacted with many different suppliers,it will waste too much time.",
            "Work with us now,let us work in more efficient way!",
            "4. Plan to build your own brand ?",
            "We have many years working experience in helping customer build their own brand, include private label, customized package, thanks cards, LOGO printing."
          ],
          img:require('@/assets/img/sourcing_2.jpg')
        },
        {
          title: "Most suitable transportation for you",
          content: [
            "1. If you order small quantity,we can deliver to you by air,such as DHL,FEDEX,TNT,UPS,Epacket,we also do dropshipping.",

            "2. If you order product in bulk with large quantity, we can deliver to you by sea,train,truck,we do EXW,FOB,CFR,CIF,DDP,etc.",
            "We offer national collect goods service,can collect goods from Yiwu,Ningbo,Shenzhen,Hongkong,etc.",
            "We can do export customs clearance, import customs clearance,do import tax free and door to door service.",
            "We can provide imported document,such as Certificate of Origin (C/O), Form E, Form A service,Export License."
          ],
          img:require('@/assets/img/sourcing_3.jpg')
        }
      ]
    };
  },
  mounted() {
    var wow = new WOW();
    wow.init();
  },
  methods: {
    clickBlog(item) {
      // this.$router.push('/blogdetail')
    }
  }
};
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner1.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
.container{
  padding-bottom: 50px;
}
.row {
  margin-right: 0;
  margin-left: 0;
}
.CompanyIntroduction-container {
  padding: 0px 0;
  color: #808080;
  transition: all ease 0.5s;
}
.CompanyIntroduction-container > div > p {
  font-size: 14px;
  /* line-height: 2.5rem; */
}
@media screen and (max-width: 997px) {
  .CompanyIntroduction-container {
    padding: 10px 0;
    color: #808080;
  }
}
</style>

