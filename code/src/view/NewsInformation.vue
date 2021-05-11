<template>
    <div id="NewsInformation">
        <div class="container">
            <div class="container text-center">
                <h3>News</h3>
                <!-- <p style="color:#b2b2b2">Company News</p> -->
            </div>
            <!-- <div class="nav container text-center">
                <a href="#" class="active">公司新闻</a>
                <a href="#">行业动态</a>
            </div> -->
            <ul class="news-container container-fuild">
                <li v-for="(item,index) in newsList" :key="index" class="wow fadeIn">
                    <div class="content">
                        <p>{{item.title}}</p>
                        <p>{{item.introduce}}</p>
                    </div>
                    <div class="time">
                        <p>{{item.date}}</p>
                        <span>{{item.year}}</span>
                    </div>
                    <div class="circle">
                        <img src="../assets/img/circle.png">
                        <i class="line center-block"></i>
                    </div>
                </li>
            </ul>
            <div class="contaianer-fuild text-center more">
                <i class="glyphicon glyphicon-th"></i>
            </div>
        </div>
    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'NewsInformation',
    data(){
        return{
            newsList:[
                {
                    id: '001',
                    title: 'Suez Canal ship freed, but the pressure points in supply chain, global trade persist ',
                    introduce: '',
                    date: '03-29',
                    year: '2021'
                },{
                    id: '002',
                    title: "USA TODAY's expert panel says vaccine delivery must double to reach most Americans in summer and bring pandemic relief. Progress slowed in early 2021. ",
                    introduce: '',
                    date: '03-18',
                    year: '2021'
                },{
                    id: '003',
                    title: "In 2020, online retail platform Amazon reported a net income of 21.33 billion U.S. dollars, up from a 11.6 billion U.S. dollar net income in the previous year. During the same fiscal period, the company's revenue amounted to more than 386 billion U.S. dollars.",
                    introduce: '',
                    date: '01-10',
                    year: '2021'
                },{
                    id: '004',
                    title: 'VAT Changes on Sales to UK Customers on Amazon for 2021',
                    introduce: '',
                    date: '12-24',
                    year: '2020'
                },{
                    id: '005',
                    title: 'The United Kingdom left the European Union on 31 January 2020. In 2020 the EU and the UK reached an agreement on their new partnership. It sets out the rules that apply between the EU and the UK as of 1 January 2021. ',
                    introduce: '',
                    date: '01-31',
                    year: '2020'
                },{
                    id: '006',
                    title: 'According to the latest news, a container ship full of Chinese cargo, INTERASIA CATALYST ship during the voyage, the ship loaded with containers suddenly caught fire, the fire was once out of control! Industry analysts believe that the container ship fire accident is very likely to be dangerous goods or flammable goods reported caused. ',
                    introduce: '',
                    date: '01-20',
                    year: '2020'
                }
            ]
        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    },
}
</script>
<style scoped>
.nav{
    margin: 20px 0;
}
.nav>a{
    display: inline-block;
    text-decoration: none;
    width: 120px;
    height: 45px;
    line-height: 45px;
    color: #333;
    border: 1px solid #333;
}
.nav>a.active{
    color: #1e73be;
    border-color: #1e73be;
}
.nav>a:hover{
    color: #1e73be;
    border-color: #1e73be;
}
.news-container{
    overflow: hidden;
    margin-bottom: 0;
}
.news-container>li{
    width: 55.6%;
    height: 120px;
    float: left;
    color: #333;
    text-align: right;
    border-left: 1px solid transparent;
    border-right: 1px solid transparent;
}
.news-container>li:hover{
    color: #1e73be;
    border: 1px solid #1e73be;
    cursor: pointer;
}
.news-container>li:nth-of-type(2n){
    float: right;
    text-align: left;
}
.news-container>li>.content{
    width: 60%;
    float: left;
    padding: 20px 0;
}
.news-container>li>.time{
    width: 20%;
    float: left;
    padding: 10px 0;
}
.news-container>li>.time>p{
    font-size: 30px;
    margin: 5px 0;
}
.news-container>li>.circle{
    width: 20%;
    height: 100%;
    float: left;
    position: relative;
}
.news-container>li>.circle>img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    width: 20px;
    height: 20px;
}
.news-container>li>.circle>i{
    display: block;
    width: 1px;
    height: 100%;
    background: #707070;
}
.news-container>li:nth-of-type(2n)>.content{
    float: right;
}
.news-container>li:nth-of-type(2n)>.time{
    float: right;
}
.news-container>li:nth-of-type(2n)>.circle{
    float: right;
}
.news-container>li:nth-of-type(1)>.circle>i{
    height: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
}
.more{
    font-size: 25px;
    color: #707070;
}
.more>i{
    cursor: pointer;
}
@media screen and (max-width: 767px){
    .news-container>li{
        width: 100%;
    }
    .news-container>li>.content{
        width: 70%;
        text-align: left;
        float: right;
    }
    .news-container>li>.time{
        width: 30%;
        text-align: left;
        float: right;
    }
    .news-container>li>.circle{
        display: none;
    }
}
</style>

