<template>
    <div class="header">
        <div class="inner">
            <div class="demo1"><img src="./../images/logo.jpg" alt=""></div>
            <div class="demo2"><a href="" v-for="item in caidan" :key="item.id">{{item}}</a></div>
            <div class="demo3"><form action="" method="get">
                <input type="search" name="search" placeholder=" 请输入关键字...">
                <img id="fdj" src="./../images/搜索图标.png" alt="">
            </form>
            </div>
            <div class="demo4"><a href="">登录 |</a>
                <a href=""> 注册</a></div>
            <div class="demo5">
                <img src="./../images/右上角logo1.jpg" alt="">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'nav-header',
    data: function(){
        return{
            caidan:['首页','课程','Java','我的',]
        }
    }
}
</script>

<style>
    .header{
        position: absolute;
        top: 0px;
        width: 100%;
        height: 78px;
        line-height: 78px;
        box-shadow: 0px 10px 10px #DCF2E5;
    }
    .inner{
        position: relative;
        width: 90%;
        height: 100%;
        line-height: 100%;
        margin: 0 auto;
    }
    
    .demo2 a{
        position: relative;
        color: black;
        font-size: 22px;
        text-decoration: none;
        margin-left: 52px;
        display: inline;
    }
    form{
        position: relative;
    }
 
        
    .demo1,.demo2,.demo3,.demo4,.demo5{
        height: 100%;
        position: relative;
        float: left;
    }
    .demo1{
        width: 15%;
    }
    .demo1 img{
        width: 100%;
        height: 68px;
    }
    .demo2{
        width: 36%;
        top: 30px;
    }
    .demo3{
        width: 30%;

    }
    .demo3 input{
        position: relative;
        top: 15px;
        left: 50px;
        height: 38px;
        width: 80%;
        font-size: 16px;
        background-color: #E9E9E9;
        border-radius: 8px;
        border:none;
    }
      .demo3 #fdj{
        position: relative;
        width: 30px;
        height: 30px;
        right: -20px;
        top: 30px;
    }
    .demo4{
        width: 12%;
    }
    .demo4 a{
        position:relative;
        top: 30px;
        color: gray;
        text-decoration: none;
    }
     .demo5{
         width:4%;
    }
    .demo5 img{
        position: relative; 
        top: 18px;
        left: 50%;
        width: 100%;
        height: 60%;
        border: 1px solid black;
        border-radius: 50%;
        right: 0px;

    }
</style>