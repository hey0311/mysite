<template>
  <div id="ContactUs">
    <div class="banner container-fuild text-center"></div>
    <div class="container">
      <div class="container-fuild ContactUs-container">
        <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-6 form-wrapper" :style="{marginRight:'20px'}">
            <form class="form-horizontal" role="form" @submit.prevent="sendEmail">
              <div class="form-group">
                <label for="name" class="col-sm-2 control-label" >Name</label>
                <div class="col-sm-10 col-xs-12">
                  <input type="text" class="form-control" id="name" v-model="name" name="from_name"/>
                </div>
              </div>
              <div class="form-group">
                <label for="email" class="col-sm-2 control-label">Email</label>
                <div class="col-sm-10">
                  <input type="text" class="form-control" id="email" v-model="email" name="from_email"/>
                </div>
              </div>
              <div class="form-group">
                <label for="tel" class="col-sm-2 control-label">Tel</label>
                <div class="col-sm-10">
                  <input type="text" class="form-control" id="tel"  v-model="tel" name="from_tel"/>
                </div>
              </div>
              <div class="form-group">
                <label for="content" class="col-sm-2 control-label" >Message</label>
                <div class="col-sm-10">
                  <textarea class="form-control" id="content" rows="8" v-model="message" name="message"></textarea>
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
              <img class="company-icon" src="@/assets/img/company.png" />
              <div
                class="company-name"
                :style="{fontWeight:'bold'}"
              >Shenzhen April Spring Technology Co.,Ltd</div>
            </div>
            <div class="company">
              <img class="company-icon" src="@/assets/img/whatsapp.png" />
              <div class="company-name">(0086+)13691663387</div>
            </div>
            <div class="company">
              <img class="company-icon" src="@/assets/img/email.png" />
              <div class="company-name">sales06@buyshiphere.com</div>
            </div>
            <div class="company">
              <img class="company-icon" src="@/assets/img/skype.png" />
              <div class="company-name">monica@apriltec.com</div>
            </div>
            <div class="company" style="align-items:flex-start">
              <img class="company-icon" src="@/assets/img/wechat.png" />
              <div class="company-name-wrapper">
                <div class="company-name">fangcuizhu</div>
                <img
                  class="company-name"
                  style="width:100px;height:100px"
                  src="@/assets/img/wechatcode.jpg"
                />
              </div>
            </div>
            <div class="company">
              <img class="company-icon" src="@/assets/img/qq.png" />
              <div class="company-name">2485068656</div>
            </div>
            <div class="company">
              <img class="company-icon" src="@/assets/img/clock.png" />
              <div class="company-name-wrapper">
                <div class="company-name">Mon to Sat 09:00 - 19:00</div>
                <!-- <div class="company-name" :style="{fontWeight:'bold'}">Sunday CLOSED</div> -->
              </div>
            </div>
            <div class="company" style="align-items:flex-start">
              <img class="company-icon" src="@/assets/img/address.png" />
              <div class="company-name-wrapper">
                <div class="company-name" :style="{fontWeight:'bold'}">ShenZhen,China</div>
                <div
                  class="company-name"
                >Room 303, Building C, No. 9, Yuanchuang Park, Longwu Industrial Zone, Bulong Road, Shangfen Community, Minzhi Street, Longhua District, Shenzhen, Guangdong</div>
                <iframe
                  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d920.59207349766!2d114.01795085553165!3d22.640053081317497!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x34038cc40c983a9f%3A0x3c08fc5c323fd487!2z6b6Z5pi85bel5Lia5Yy6!5e0!3m2!1seh-US!2sjp!4v1620753073570!5m2!1sen-US!2sjp"
                  width="600"
                  height="450"
                  style="border:0;"
                  allowfullscreen
                  class="google-map"
                  loading="lazy"
                ></iframe>
              </div>
            </div>
            <!-- <div class="col-xs-12 col-sm-12 col-md-6" :style="{marginTop:'10px',float:'right',padding:0}">
              <div id="map" class="wow zoomIn"></div>
            </div>-->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from "wowjs";
import emailjs from 'emailjs-com';
import axios from 'axios'
import{ init } from 'emailjs-com';
export default {
  name: "ContactUs",
  data() {
    return {
      name:'',
      email:'',
      tel:'',
      message:''
    };
  },
  methods: {
    sendEmail(e) {
      var url = 'https://sctapi.ftqq.com/SCT38230Toz3KPGlvGVX1JAHFhzvucbgf.send?title='+encodeURI('buyshiphere message')+'&desp='+encodeURI(
        'name:'+this.name+
        '\n,email:'+this.email+
        '\ntel:'+this.tel+
        '\nmessage:'+this.message
      )
      axios.get(url).then(function(res){
        // alert('send success!')
      }).catch(function(err){
        // alert('send fail!')
      })
      emailjs.sendForm('service_qyujneg', 'template_td08evi', e.target, 'user_9lxO7oP1kofmIY4hRMRZU')
        .then((result) => {
            console.log('SUCCESS!', result.status, result.text);
            window.alert('SUCCESS!')
        }, (error) => {
            console.log('FAILED...', error);
            window.alert('FAILED...')
        }); 
    }
  },
  mounted() {
    init("user_9lxO7oP1kofmIY4hRMRZU");
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
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
.company-icon {
  width: 50px;
  height: 50px;
}
.company-name {
  font-size: 18px;
  margin-left: 30px;
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
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}
@media screen and (max-width: 997px) {
  .ContactUs-container {
    padding: 20px 0;
  }
}
.form-wrapper {
  flex: 0 0 50%;
}
.google-map {
  margin-left: 30px;
}
</style>

