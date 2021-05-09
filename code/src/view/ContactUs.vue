<template>
  <div id="ContactUs">
    <div class="banner container-fuild text-center"></div>
    <div class="container">
      <div class="container-fuild ContactUs-container">
        <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-6" :style="{marginRight:'20px'}">
            <form class="form-horizontal" role="form">
              <div class="form-group">
                <label for="name" class="col-sm-2 control-label">Name</label>
                <div class="col-sm-10 col-xs-12">
                  <input type="text" class="form-control" id="name" />
                </div>
              </div>
              <div class="form-group">
                <label for="email" class="col-sm-2 control-label">Email</label>
                <div class="col-sm-10">
                  <input type="text" class="form-control" id="email" />
                </div>
              </div>
              <div class="form-group">
                <label for="tel" class="col-sm-2 control-label">Tel</label>
                <div class="col-sm-10">
                  <input type="text" class="form-control" id="tel" />
                </div>
              </div>
              <div class="form-group">
                <label for="content" class="col-sm-2 control-label">Message</label>
                <div class="col-sm-10">
                  <textarea class="form-control" id="content" rows="8"></textarea>
                </div>
              </div>
              <div class="form-group">
                <div class="col-sm-offset-2 col-sm-10">
                  <button type="submit" class="btn btn-default btn-block">Send</button>
                </div>
              </div>
            </form>
          </div>
          <div class="contact-wrapper">
            <div class="contact">Contact Information</div>
            <div class="sub-text1">
              <span :style="{fontWeight:'bold'}">Usually</span>, you will get reply within 24 Hours after you contacted us. Any information from you is warmly welcome.Please do not hesitate to contact us!
            </div>
            <div class="sub-text2">We’d love to hear from you and let us work together.</div>
            <div class="company">
              <div class="company-icon"></div>
              <div class="company-name" :style="{fontWeight:'bold'}">dropshipnow</div>
            </div>
            <div class="company">
              <div class="company-icon"></div>
              <div class="company-name">(0086+)13691663387</div>
            </div>
            <div class="company">
              <div class="company-icon"></div>
              <div class="company-name">info@buyshipnow.com</div>
            </div>
            <div class="company">
              <div class="company-icon"></div>
              <div class="company-name">Mon to Sat 09:00 - 19:00</div>
              <div class="company-name" :style="{fontWeight:'bold'}">Sunday CLOSED</div>
            </div>
            <div class="company">
              <div class="company-icon"></div>
              <div class="company-name" :style="{fontWeight:'bold'}">ShenZhen,China</div>
              <div
                class="company-name"
              >6th Floor, Building A17, 4th District, Huai De Cuigang Industrial Park, Fuyong, Baoan District, Shenzhen,China</div>
            </div>
            <!-- <div class="col-xs-12 col-sm-12 col-md-6" :style="{marginTop:'10px',float:'right',padding:0}">
              <div id="map" class="wow zoomIn"></div>
            </div> -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from "wowjs";
// import BMap from "BMap";
export default {
  name: "ContactUs",
  data() {
    return {};
  },
  mounted() {
    // var map = new BMap.Map("map"); // 创建地图实例
    // var point = new BMap.Point(116.301841, 40.156506); // 创建点坐标
    // map.centerAndZoom(point, 18); // 初始化地图，设置中心点坐标和地图级别
    // map.enableScrollWheelZoom(true); //开启鼠标滚轮缩放
    // var marker = new BMap.Marker(point); // 创建标注
    // map.addOverlay(marker); // 将标注添加到地图中
    // var opts = {
    //   width: 50, // 信息窗口宽度
    //   height: 10, // 信息窗口高度
    //   title: "黄元公寓" // 信息窗口标题
    // };
    // var infoWindow = new BMap.InfoWindow("我的家", opts); // 创建信息窗口对象
    // map.openInfoWindow(infoWindow, map.getCenter()); // 打开信息窗口
    // var wow = new WOW();
    // wow.init();
  }
};
</script>
<style scoped>
.control-label {
  font-size: 18px;
}
.contact-wrapper {
  margin-left: 30px;
}
.contact {
  font-size: 30px;
  font-weight: bold;
}
.sub-text1 {
  font-size: 18px;
}
.sub-text2 {
  font-weight: bold;
  font-size: 18px;
}
.company {
  margin-top: 10px;
}
.company-name {
  font-size: 18px;
  /* font-weight: bold; */
}
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner_1.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
.ContactUs-container {
  padding: 80px 0;
  transition: all ease 0.5s;
  box-sizing: border-box;
}
#map {
  width: 100%;
  height: 365px;
}
.row {
  margin-right: 0;
  margin-left: 0;
}
@media screen and (max-width: 997px) {
  .ContactUs-container {
    padding: 20px 0;
  }
}
</style>

