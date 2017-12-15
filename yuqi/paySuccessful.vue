<template>
    <div>
        <header>
            <div class="main">
                <div class="left">
                    <div class="logo">
                    </div>
                    <ul class="nav">
                        <li><a href="">首页</a></li>
                        <li><a href="">产品中心</a></li>
                        <li><a href="">品牌介绍</a></li>
                    </ul>
                </div>
                <div class="right">
                    <ul class="shop">
                        <li>购</li>
                        <li><img src="../../assets/images/my2.png" alt=""></li>
                    </ul>
                </div>
            </div>
        </header>
        <section class="liucheng">
            <div class="left">
                <div class="top">
                    <div class="name">支付成功</div>
                    <div class="yuan">
                        <span></span>
                        <ul class="dian">
                            <li></li>
                            <li></li>
                            <li></li>
                        </ul>
                    </div>
                </div>
                <div class="center">SHOPPING</div>
                <div class="bottom">
                    <div class="name">CART</div>
                    <div class="logo"></div>
                </div>
            </div>
            <div class="right">
                <div class="process">
                    <li>
                        <div class="waiyuan">
                            <div class="neiyuan">壹</div>
                        </div>
                        <div class="name">购物车</div>
                    </li>
                    <li>
                        <div class="waiyuan">
                            <div class="neiyuan">贰</div>
                        </div>
                        <div class="name">订单</div>
                    </li>
                    <li>
                        <div class="waiyuan">
                            <div class="neiyuan">叁</div>
                        </div>
                        <div class="name">付款</div>
                    </li>
                    <li>
                        <div class="waiyuan">
                            <div class="neiyuan active">肆</div>
                        </div>
                        <div class="name">完成</div>
                    </li>
                </div>
                <div class="line">
                    <div></div>
                    <div></div>
                    <div></div>
                </div>
            </div>
        </section>
        <section class="carlist" style="height: 200px;">
            <div class="huabi"><img src="../../assets/images/huabi.png" alt=""></div>
            <div class="title">您的订单已提交成功，现在就去付款吧~ <span>&nbsp;ORDER SUCCESSFUL</span></div>
            <ul class="content" style="width:100%;height: 115px;">
                <div class="left" style="width:30px;height: 100%;float: left;"><div class="logo1" style="width:30px;height:35px;background:url('../../assets/images/bianji.png') no-repeat center/cover;margin-right: 20px;"></div></div>
                <div class="right" style="display: flex;justify-content: space-between;flex-direction: column;float: left; color:#525252;">
                    <p>您的订单号：<span style="color:#4499EF;">1761178637</span>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;应付金额：&nbsp;&nbsp;&nbsp;<span style="color:#D20B1F;">324.<span style="font-size: 14px;">00RMB</span></span> </p>
                    <p>支付方式：在线支付</p>
                    <p>送货时间：工作日、双休日和节假日均送货</p>
                </div>
            </ul>
            <div class="address">HI!黑子，如果2小时内您无法完成付款，系统会将您的订单取消。</div>
        </section>
        <section class="tuijian">
            <div class="title">- &nbsp;&nbsp;&nbsp;相关推荐&nbsp;&nbsp;&nbsp; -</div>
            <ul>
                <li>
                    <img src="../../assets/images/500135738_banner.png" alt="">
                    <span>紫檀柳佛珠手串</span>
                    <span>新鲜出炉/抗压耐磨/专业品质</span>
                </li>
                <li>
                    <img src="../../assets/images/500135738_banner.png" alt="">
                    <span>紫檀柳佛珠手串</span>
                    <span>新鲜出炉/抗压耐磨/专业品质</span>
                </li>
                <li>
                    <img src="../../assets/images/500135738_banner.png" alt="">
                    <span>紫檀柳佛珠手串</span>
                    <span>新鲜出炉/抗压耐磨/专业品质</span>
                </li>
            </ul>
        </section>
        <footer>
            <div class="top">
                <ul class="dibu">
                    <li class="li1">
                        <p>联系方式</p>
                        <p><b>CONTACT</b></p>
                        <span><b>400-659-900</b></span>
                    </li>
                    <li class="li2">
                        <p>常见问题</p>
                        <p><b>PROBLEM</b></p>
                        <ul class="wenzi">
                            <li><a href="">购物问题</a></li>
                            <li><a href="">物流问题</a></li>
                            <li><a href="">支付问题</a></li>
                            <li><a href="">售后问题</a></li>
                            <li><a href="">其它问题</a></li>
                        </ul>
                    </li>
                    <li class="li3">
                        <p>联系方式</p>
                        <p><b>NAVIGATION</b></p>
                        <ul class="wenzi">
                            <li><a href="">热门精选</a></li>
                            <li><a href="">折扣专区</a></li>
                            <li><a href="">会员专区</a></li>
                            <li><a href="">本周精选</a></li>
                            <li><a href="">全部商品</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div class="bottom">
                RE-CIKL MUX, powered by alimama THX.法律声明   转载内容版权归作者及来源网站所有，商业媒体及纸媒请先联系：sangxing@taobao.com
            </div>
        </footer>
    </div>
</template>
<script>
    export default {
        name:'gouwuche',
        data() {
            return {
                radio:'',
                tableData: [{
                    date: '2016-05-02',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                }, {
                    date: '2016-05-04',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1517 弄'
                }, {
                    date: '2016-05-01',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1519 弄'
                }, {
                    date: '2016-05-03',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1516 弄'
                }]
            }
        },
        /*methods:{
            ///////反选/////////
            reverSelection() {
                this.tableData.forEach(row => {
                    this.$refs.multipleTable.toggleRowSelection(row);
                });
            },
            ///////取消选择///////
            cancel(){
                this.$refs.multipleTable.clearSelection();
            },
            //////////多选//////////
            handleSelectionChange(val) {
                this.multipleSelection = val;
            },
            //////////删除选中的//////////
            del(){
                let ids=this.multipleSelection.map(ele=>ele.id);
                this.$http.post('/home/moniDelete.php',{ids}).then(res=>{
                    if(res.body =='ok'){
                        this.$message({
                            showClose: true,
                            message:'删除成功',
                            type:"success"
                        })
                        this.tableData =  this.tableData.filter(ele=>!ids.includes(ele.uid));
                    }else if(res.body =='error'){
                        this.$message({
                            showClose: true,
                            message: '删除失败',
                            type: 'error'
                        });
                    }
                })
            }
        },
        mounted(){
            this.$http.post('/home/manageMoni.php').then(res=>{
                this.tableData=res.body;
            });
        }*/
    }
</script>
<style>
    *{
        margin: 0;
        padding: 0;
        list-style: none;
        text-decoration: none;
    }
    *{
        -webkit-tap-hightlight-color: rgba(0, 0, 0, 0);
        -webkit-text-size-adjust: none;
        -webkit-box-sizing: border-box;
        box-sizing: border-box;
    }
    body{
        background: #fff;
    }
    a{
        text-decoration: none;
    }
    header{
        width: 100%;
        height:80px;
        margin-top: 20px;
        margin-bottom: 32px;
    }
    .main{
        width: 1200px;
        height:100%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    header .left{
        width: 1063px;
        height: 100%;
        background: #7CCABA;
        border-radius: 5px;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .logo{
        width: 100px;
        height: 100%;
        background: url("../../assets/images/LOGO.png") no-repeat center/cover;
        margin-left: 60px;
    }
    .nav{
        width: 700px;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .nav>li{
        padding: 0 10px;
    }
    .nav>li>a{
        color: #FFFFFF;
        font-size: 16px;
        font-weight: 700;
    }
    header .right{
        width: 137px;
        height:52px;
        background: #7CCABA;
        border-radius: 4px;
    }
    .shop{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .shop>li{
        width:34px;
        height:34px;
        border:2px solid #E51217;
        border-radius: 50%;
    }
    .shop>li:first-child{
        color: #FFFFFF;
        font-size: 14px;
        text-align: center;
        background: #E51217;
        line-height: 34px;
    }
    .shop>li:last-child{
        color: #FFFFFF;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .shop>li:last-child>img{
        width: 20px;
        height:20px;

    }
    .liucheng{
        width:1200px;
        height: 90px;
        margin:0 auto;
    }
    .liucheng .left{
        width:125px;
        height: 75px;
        flex-direction: column;
        display: flex;
        justify-content: space-between;
        float:left;
    }
    .liucheng .left .top{
        flex:1;
        align-content: flex-end;
        position: relative;
    }
    .liucheng .left .top .yuan{
        display: flex;
        justify-content: space-between;
        flex-direction: column;
    }
    .liucheng .left .top .name{
        color:#000;
        font-size: 24px;
        float: left;
        margin-right: 8px;
    }
    .liucheng .left .top .yuan span{
        flex:1;
        align-items: flex-start;
        height:20px;
    }
    .liucheng .left .top .yuan ul{
        width:25px;
        height: 6px;
        flex:1;
        align-items: flex-end;
        float: left;
        display: flex;
        justify-content: space-between;
    }
    .liucheng .left .top .dian li{
        width:6px;
        height:6px;
        border-radius: 50%;
        margin-right: 4px;
        flaot:left;
    }
    .liucheng .left .top .dian li:first-child{
        background: #7BCBB9;
    }
    .liucheng .left .top .dian li:nth-child(2){
        background: #BDE5DC;
    }
    .liucheng .left .top .dian li:last-child{
        background: #E5F5F1;
    }
    .liucheng .left .center{
        color:#7BCBB9;
        font-size: 18px;
        flex:1;
        align-content: flex-end;
    }
    .liucheng .left .bottom{
        color:#DC5876;
        display: flex;
        justify-content: space-between;
        position: relative;
    }
    .liucheng .left .bottom .logo{
        width:18px;
        height:18px;
        background: url("../../assets/images/gouwuche.png") no-repeat center/cover;
        position: absolute;
        top:0;
        right:60px;
    }
    .liucheng .right{
        width:403px;
        height: 67px;
        float:right;
        margin-top: 23px;
        position: relative;
    }
    .right .process{
        width:403px;
        height: 67px;
        display: flex;
        justify-content: space-between;
    }
    .right .process li{
        width:52px;
        height:67px;
        padding-top:2px;
        position: relative;
    }
    .right .process li .waiyuan{
        width:44px;
        height:44px;
        border:2px solid #7BC0B1;
        border-radius: 50%;
        background: #fff;
        margin-left:4px;
        position: relative;
        margin-bottom: 4px;
    }
    .right .process li .neiyuan{
        width:36px;
        height:36px;
        background: #8AC7B9;
        border-radius: 50%;
        position:absolute;
        top:50%;
        left:50%;
        margin-top: -18px;
        margin-left:-18px;
        text-align: center;
        line-height: 36px;
        font-size: 16px;
    }
    .right .process li .neiyuan.active{
        background: #EDF59D;
    }
    .right .process li .name{
        width:100%;
        color:#7FCDBB;
        text-align: center;
        font-size: 16px;
    }
    .liucheng .right .line{
        width:286px;
        height: 2px;
        position: absolute;
        left:57px;
        top:23px;
        display: flex;
        justify-content: space-between;
    }
    .liucheng .right .line div{
        width:50px;
        height: 100%;
        background: #7BCBB9;
    }
    .carlist{
        width:1200px;
        height: 360px;
        margin:80px auto;
        padding:10px 21px 0 21px;
        position:relative;
        background: #fff;
    }
    .carlist .huabi {
        width:110%;
        height: 72px;
        position: absolute;
        left:-25px;
        top:-45px;
        z-index: -1;
    }
    .carlist .huabi img{
        display: block;
        width:100%;
        height: 100%;
    }
    .carlist .operate{
        width:50px;
        height:24px;
        /*background: red;*/
        display: flex;
        justify-content: space-between;
    }
    .carlist .title{
        width:100%;
        height:53px;
        background: #fff;
        line-height: 53px;
        font-size:24px;
        color:#7D7D7D;
        border-bottom: 1px dashed #C9C9C9;
        padding-left:20px;
    }
    .carlist .title span{
        font-size: 18px;
    }
    .carlist .content{
        width:100%;
        height: auto;
        padding-top: 37px;
    }
    .carlist .content .line{
        width:900px;
        height: 20px;
        margin-bottom: 30px;
    }
    .carlist .content .line .sort{
        display: flex;
        justify-content: space-between;
    }
    .carlist .address{
        width:552px;
        height:42px;
        background: #E53842;
        border-radius: 0 8px 8px 8px ;
        text-align: center;
        line-height: 38px;
        font-size: 18px;
        color:#fff;
    }
    .selectAll{
        width:18px;
        height: 18px;
        background: #E7E7E7;
        border-radius: 50%;
        margin-top: 2px;
        border:5px solid #C9C9C9;
        box-sizing: border-box;
        float:left;
    }
    .selectAll.actives{
        background: #2D8BEC;
    }
    .sort .phone .logo{
        width:18px;
        height: 18px;
        background: url("../../assets/images/bianji.png") no-repeat center/cover;
        margin-right: 24px;
    }
    .sort .phone ,.sort .location{
        display: flex;
        justify-content: space-between;
    }
    .sort .moren{
        width:70px;
        margin-left: 10px;
        margin-right: 30px;
        color:#3E8FF3;
        font-weight: 600;
    }
    .sort .location .logo{
        width:18px;
        height: 18px;
        background: url("../../assets/images/local.png") no-repeat center/cover;
        margin-right: 14px;
    }
    .operate .shanchu{
        width:24px;
        height: 24px;
        background: url("../../assets/images/shanchu.png") no-repeat center/cover;
        margin-left:-15px;
    }
    .operate .bianji{
        width:18px;
        height: 18px;
        background: url("../../assets/images/bianji.png") no-repeat center/cover;
        margin-top: 3px;
    }
    .submit{
        width:100%;
        height: 200px;
        display: flex;
        justify-content: space-between;
        flex-direction: column;
        margin-top: 180px;
    }
    .submit div:last-child{
        width:312px;
        height: 68px;
        background: #72C7B4;
        border-radius: 30px;
        text-align: center;
        line-height: 68px;
        color:#fff;
        font-size: 32px;
    }
    .tuijian{
        width: 100%;
        height: auto;
        margin-bottom: 70px;
    }
    .tuijian .title{
        width: 1200px;
        margin:50px auto;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #7bcbb9;
        font-weight: 800;
    }
    .tuijian>ul{
        width: 1200px;
        height: auto;
        margin:0 auto;
        display: flex;
        justify-content: space-between;
    }
    .tuijianul>ul>li{
        padding:20px 0;
        display: flex;
        justify-content: center;
    }
    .tuijian>ul>li>img{
        width: 305px;
        height:240px;
    }
    .tuijian>ul>li>span{
        display: block;
        margin-bottom: 10px;
        text-align: center;
        color: #343434;
    }
    .tuijian>ul>li>span:last-of-type{
        color: #8d8d8d;
        font-size: 14px;
    }
    footer{
        width:100%;
        height:350px;
    }
    footer .top{
        width:100%;
        height:282px;
        background:#2a302e;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    footer .top .dibu{
        width:831px;
        height:175px;
        display: flex;
        justify-content:space-between;
        align-items: center;
    }
    footer .top .dibu li{
        float: left;
    }
    footer .top .dibu li p{
        margin-bottom: 7px;
    }
    footer .top .dibu li p:nth-of-type(1){
        color:#8b8d8c;
    }
    footer .top .dibu li p:nth-of-type(2){
        color:#e0e1e0;
    }
    footer .top .dibu .li1 span{
        font-size: 21px;
        margin-top: 30px;
        display: block;
        color: white;
    }
    footer .top .dibu .li2 .wenzi, .li3 .wenzi{
        width:57px;
        height:107px;
        display: flex;
        flex-direction: column;
        justify-content:space-around;
    }
    footer .top .dibu .li2 .wenzi li{
        width:57px;
        height:13px;
        font-size: 13px;
    }
    footer .top .dibu .li3 .wenzi li{
        width:57px;
        height:13px;
        font-size: 13px;
    }
    footer .top .dibu .li2 .wenzi li a{
        color: #7d807f;
    }
    footer .top .dibu .li3 .wenzi li a{
        color: #7d807f;
    }
    footer .top .dibu li:first-of-type{
        width:170px;
        height:100%;
    }
    footer .top .dibu li:nth-of-type(2){
        width:90px;
    }
    footer .top .dibu li:nth-of-type(3){
        width:116px;
    }
    footer .bottom{
        width:100%;
        height: calc( 350px - 282px);
        background:black;
        text-align: center;
        line-height: calc( 350px - 282px);
        font-size: 13px;
        color: #848484;
    }
</style>