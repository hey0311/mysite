<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center">关于我们</div>
        <div class="container">
            <div class="row CompanyIntroduction-container">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/logo_white.jpg">
                </div>
                <div @click="clickBlog" class="col-xs-12 col-sm-12 col-md-6">
                    <h3>Shenzhen Buyshipnow trading Co.,Ltd </h3>
                    <p class=".text-justify">Shenzhen Buyshipnow trading Co.,Ltd is located in Shenzhen China,we have worked togethere with more than 100 online sellers,including Amazon Sellers, eBay Sellers,shopify seller,etc.
When you buy from Aliexpress, you may encounter problems:
Such as high product prices, long shipping time,lost parcels in transit, high shipping costs, slowly response from supplier, etc. 
Now, let us help solve these problems !</p>
                </div>
            </div>
            <div v-for="item in list" :key="item.title" class="row CompanyIntroduction-container">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <!-- <img class="img-responsive center-block" src="@/assets/img/about_img.png"> -->
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>{{item.title}}</h3>
                    <p class=".text-justify">{{item.content}}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'CompanyIntroduction',
    data(){
        return{
            list:[{
                title:'1, Can you do label, packing?',
                content:'Yes, please provide packaging requirements.'
            },{
                title:'2, Can you help me inspect our goods?',
                content:'Yes, Please offer your detail requirements for the inspection.'
            },{
                title:'3, Can you help pick up our goods from the inland of China?',
                content:'Yes, Please offer the exact address for picking up.'
            },{
                title:'4, How can I pay you?',
                content:'You can pay us by bank transfer (T/T), Western Union , Paypal and so on.'
            },{
                title:'5, Can you ship my goods to Amazon/Europe warehouse?',
                content:'Yes,we can help to ship your goods to Amazon/Europe warehouse storing,or deliver to your door as well.'
            }]
        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    },
    methods:{
        clickBlog(item){
            this.$router.push('/blogdetail')
        }
    }
}
</script>
<style scoped>
.banner{
    color: #fff;
    font-size: 30px;
    height: 150px;
    line-height: 150px;
    background-image: url('../assets/img/banner1.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: scroll;
    background-position: center center;
}
.row{
    margin-right: 0;
    margin-left: 0;
}
.CompanyIntroduction-container{
    padding: 0px 0;
    color: #808080;
    transition: all ease 0.5s;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.CompanyIntroduction-container>div>p{
    font-size: 14px;
    line-height: 2.5rem;
}
@media screen and (max-width: 997px){
    .CompanyIntroduction-container{
    padding: 10px 0;
    color: #808080;
}
}
</style>

