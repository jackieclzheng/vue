<template>
    <div class="index">
        <div class="container">
            <div class="swiper-box">
                <swiper :options="swiperOption">
                    <swiper-slide v-for="item in slideList" :key="item.id">
                        <a :href="'/#/product'+item.id">
                        <img :src="item.img"></a>
                    </swiper-slide>
                    <div class="swiper-pagination" slot="pagination"></div>
                    <div class="swiper-button-prev swiper-button-white" slot="button-prev"></div>
                    <div class="swiper-button-next swiper-button-white" slot="button-next"></div>
                    <div class="swiper-scrollbar" slot="scrollbar"></div>
                </swiper>
            </div>
        <div class="caidan">
            <table>
                <tr><td></td><td></td></tr>
                <tr><td>数据开发</td><td>▸</td></tr>
                <tr><td colspan="2"><hr></td></tr>
                <tr><td>数据开发</td><td>▸</td></tr>
                <tr><td colspan="2"><hr></td></tr>
                <tr><td>数据开发</td><td>▸</td></tr>
                <tr><td colspan="2"><hr></td></tr>
                <tr><td>数据开发</td><td>▸</td></tr>
                <tr><td colspan="2"><hr></td></tr>
                <tr><td>数据开发</td><td>▸</td></tr>
                <tr><td colspan="2"><hr></td></tr>
                <tr><td>数据开发</td><td>▸</td></tr>
                <tr><td></td><td></td></tr>
            </table>
        </div>
        </div>
        <div class="link-box">
            <div class="link1">
                <div class="ljc">
                    <div class="content1">
                        <img class="lt" src="./../images/标题左侧装饰条.png" alt="绿条">
                        <h2>零基础就业</h2>
                        <h4>从入门到具备1年开发经验</h4>
                    </div>
                </div>
                <div class="tp">
                    <div class="zero" v-for="z in zeroList" :key="z.id">
                        <img :src="z" alt="z">
                    </div>
                </div>
            </div>
            <div class="link2"> 
                <div class="ljc">
                    <div class="content1">
                        <img class="lt" src="./../images/标题左侧装饰条.png" alt="绿条">
                        <h2>职场提升</h2>
                        <h4>1年以上开发经验系统成长</h4>
                    </div>
                </div>
                <div class="tp">
                     <div class="zhichang" v-for="z in zhichangList" :key="z.id">
                        <div class="content" :style="z.img">
                            <span><h3>{{z.msg1}}</h3></span>
                            <span><h5>{{z.msg2}}</h5></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="shizhan">
            <div class="content1">
                <img class="lt" src="./../images/标题左侧装饰条.png" alt="绿条">
                <h2>实战推荐</h2>
            </div>
            <div class="content2">
                <div class="tp" v-for="z in shizhanList" :key="z.id">
                        <img class="img1" :src="z.img">
                        <span style="color:gray">初级</span>
                        <img class="img2" src="两星.png" alt="">
                        <span style="color:red;margin-left: 20px;font-size: 25px;">￥299</span><br/>
                        {{z.msg}}
                </div>
            </div>
        </div>
        <div class="mianfei">
            <div class="content1">
                <img class="lt" src="./../images/标题左侧装饰条.png" alt="绿条">
                <h2>免费好课</h2>
            </div>
            <div class="content2">
                <div class="tp" v-for="z in shizhanList" :key="z.id">
                        <img class="img1" :src="z.img">
                        <span style="color:gray">初级</span>
                        <img class="img2" src="两星.png" alt="">
                        <span style="color:gray;margin-left: 20px;">
                            <img style="width: 20px; height: 12px;" src="学习路线查看图标.png" alt=""> 188</span><br/>
                        {{z.msg}}
                </div>
            </div>
        </div>
        <div class="xuexi">
            <div class="content1">
                <img class="lt" src="./../images/标题左侧装饰条.png" alt="绿条">
                <h2>学习路线</h2>
            </div>
            <div class="tp">
                    <div class="zhichang" v-for="z in zhichangList" :key="z.id">
                    <div class="content" :style="z.img">
                        <span><h3>{{z.msg1}}</h3></span>
                        <span><h5>{{z.msg2}}</h5></span>
                    </div>
                </div>
            </div>
        </div>
        <div class="remen">
            <div class="content1">
                <img class="lt" src="./../images/标题左侧装饰条.png" alt="绿条">
                <h2>热门课程</h2>
            </div>
            <div class="content2">
                <div class="tp" v-for="z in shizhanList" :key="z.id">
                        <img class="img1" :src="z.img">
                        <span style="color:gray">初级</span>
                        <img class="img2" src="两星.png" alt="">
                        <span style="color:red;margin-left: 20px;font-size: 25px;">￥299</span><br/>
                        {{z.msg}}
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { Swiper,SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
export default {
    name:'index',
    components:{
        Swiper,
        SwiperSlide,
    },
    data(){
        return{
            swiperOption:{
                autoplay:true,
                loop:true,
                // effect : 'fade',
                // fadeEffect: {
                //     crossFade: true,
                // },
                effect : 'cube',
                cubeEffect: {
                    slideShadows: true,
                    shadow: true,
                    shadowOffset: 100,
                    shadowScale: 0.6
                },
                // effect : 'coverflow',
                // slidesPerView: 3,
                // centeredSlides: true,
                // coverflowEffect: {
                //     rotate: 30,
                //     stretch: 10,
                //     depth: 60,
                //     modifier: 2,
                //     slideShadows : true
                // },
                // effect : 'flip',
                // flipEffect: {
                //     slideShadows : true,
                //     limitRotation : true,
                // },
                pagination: {
                    el: '.swiper-pagination',
                    clickable:true,
                },
                navigation: {
                    nextEl: '.swiper-button-next',
                    prevEl: '.swiper-button-prev',
                },
            },
            
            slideList:[
                {
                    id:'1',
                    img:'lunbo1.jpg',
                }, {
                    id:'2',
                    img:'lunbo2.jpg',
                }, {
                    id:'3',
                    img:'lunbo3.jpg',
                }, {
                    id:'4',
                    img:'lunbo4.jpg',
                },
            ],
            zeroList:[
                "java工程师.jpg",
                "前端工程师.jpg",
                "python工程师.jpg",
                "安卓工程师.jpg",
                "PHP工程师.jpg",
            ],
            zhichangList:[
                {
                    "msg1":"Java架构师",
                    "msg2":"跟随千万级项目从0到100一起成长",
                    "img":{
                        backgroundImage:
                        "url(职场提升1.png)",
                        backgroundRepeat: "no-repeat",
                        backgroundSize: "100% 100%"
                        }
                },
                {
                    "msg1":"从Java后端到全栈",
                    "msg2":"浓缩7月从工程师到CTO的10年成长历程",
                    "img":{
                        backgroundImage:
                        "url(职场提升2.png)",
                        backgroundRepeat: "no-repeat",
                        backgroundSize: "100% 100%"
                    }
                },
                   {
                    "msg1":"Java架构师",
                    "msg2":"跟随千万级项目从0到100一起成长",
                    "img":{
                        backgroundImage:
                        "url(职场提升3.png)",
                        backgroundRepeat: "no-repeat",
                        backgroundSize: "100% 100%"
                        }
                },                                 
            ],
            shizhanList:[
                {
                    "msg":"Java工程师从0到100一起成长",
                    "img":"图层 151.png"
                },
                 {
                    "msg":"Java工程师从0到100一起成长",
                    "img":"图层 152.png"
                },
                 {
                    "msg":"Java工程师从0到100一起成长",
                    "img":"图层 153.png",
                },
                  {
                    "msg":"Java工程师从0到100一起成长",
                    "img":"图层 154.png",
                },
                {
                    "msg":"Java工程师从0到100一起成长",
                    "img":"图层 151.png"
                },
                 {
                    "msg":"Java工程师从0到100一起成长",
                    "img":"图层 152.png"
                },
                 {
                    "msg":"Java工程师从0到100一起成长",
                    "img":"图层 153.png",
                },
                  {
                    "msg":"Java工程师从0到100一起成长",
                    "img":"图层 154.png",
                },
            ],
        }
    },

}
</script>

<style>
    .swiper-button-prev{
        margin-left: 22%;
    }
    .swiper-button-next{
        margin-right: 15%;
    }
    .container{
        --swiper-theme-color: white;
        position: relative;
        top:68px;
        margin: 0 6%;
        height: 376px;
    }
    .swiper-box{
        width: 100%;
        
    }
    img{
        border-radius: 15px;
        width: 100%;
        height: 376px;
    }
    .caidan{
        position: relative;
        border-radius: 15px 0 0 15px;
        width: 20%;
        top: -380px;
        height: 100%;
        z-index: 19;
        background: rgba(0, 0, 0, 0.2);
    }
    .caidan table{
        font-size: 18px;
        width: 100%;
        height: 100%;
        color: white;
    }
    .link-box{
        position: relative;
        top: -10px;
        width: 88%;
        margin:6% auto;
        height: 425px;
        box-shadow: 0px 10px 10px 0px #DCF2E5;
    }
    .link-box .link1{
        width: 100%;
        height: 50%;
    }
    .ljc,.tp{
        position: relative;
        width: 100%;
        height: 50%;
        border: 1px solid rgba(255, 255, 255, 0);
    }
    .content1{
        position: relative;
        height: 25px;
        margin: 40px auto 35px 0px;
    }
    .content1 .lt{
        position: absolute;
        width: 5px;
        height: 25px;
        left: 0px;
        float: left;
    }
    h2{
        position: absolute;
        font-size: 25px;
        left: 40px;
        line-height: 100%;
        display: inline;
    }
    h4{
        position:absolute;
        display: inline;
        left: 200px;
        bottom: 0px;
        color: grey;
    }
    .link-box .link2{
        width: 100%;
        height: 50%;
    }
    .zero img{
        position: relative;
        float: left;
        width: 19.1%;
        height: 90px;
        margin-left: 10px;
    }
    .zhichang .content{
        position: relative;
        float: left;
        color: white;
        width: 32.4%;
        height: 80px;
        margin-left: 10px;
    }
    .zhichang .content span{
        display: block;
        margin-top: 10px;
    }
    .shizhan,.mianfei,.xuexi,.remen{
        position: relative;
        top: -80px;
        margin: 0px auto;
        width: 88%;
        border: 1px solid white;
        height: 560px;
        margin-bottom: 10px;
    }
    .shizhan,.xuexi{
        background-color: #E9E9E9;
    }
    .mianfei,.remen{
        box-shadow: 0px 10px 10px -0px #DCF2E5;
    }
    .content2 .tp{
        position: relative;
        float: left;
        width: 23.94%;
        height: 200px;
        padding: 0px 0px 30px 10px;
    }
    .content2 .tp .img1{
        width: 100%;
        height: 75%;
    }
    .content2 .tp .img2{
        width: 40%;
        height: 15px;
        margin-left: 10px;
    }

</style>