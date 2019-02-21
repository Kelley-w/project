<template>
	<div id="my">
		<div class="top">
			<div class="top-right">
				<img src="../../assets/my/myset.jpg" />
				<img src="../../assets/my/myinfo.jpg" />
			</div>
			<div class="top-left">
				<div class="top-head">
					<img src="../../assets/my/avatar.jpg" />
				</div>
				<router-link :to="{name:'login'}">
					<p class="top-login">登录/注册</p>
				</router-link>
			</div>
		</div>
		<div class="my_order">
			<span>我的订单</span><span class="my_allorder">全部订单</span>
		</div>
		<div class="goodsStatus">
			<my-center :myStatusInfo="myStatus"></my-center>
		</div>
		<div class="myMember">
			<my-center :myStatusInfo="myMember"></my-center>
		</div>
	</div>
</template>

<script>
import myCenter from '@/components/my/my_center';
import register from '@/components/my/register'
export default{
	components:{
		myCenter,
		register
	},
	data(){
		return{
			myStatus:[
				{
					img:require('../../assets/my/index-02.png'),
					txt:'待确认'
				},
				{
					img:require('../../assets/my/index-03.png'),
					txt:'待付款'
				},
				{
					img:require('../../assets/my/index-04.png'),
					txt:'待出游'
				}
			],
			myMember:[
				{
					img:require('../../assets/my/item-01.png'),
					txt:'我的会员卡'
				},
				{
					img:require('../../assets/my/item-06.png'),
					txt:'我的优惠券'
				},
				{
					img:require('../../assets/my/item-02.png'),
					txt:'我的关注'
				},
				{
					img:require('../../assets/my/item-03.png'),
					txt:'基本资料'
				},
				{
					img:require('../../assets/my/item-05.png'),
					txt:'客服中心'
				},
				{
					img:require('../../assets/my/item-07.png'),
					txt:'常用旅客'
				}
			]
		}
	}
}
</script>

<style scoped>
#my{
	width: 100%;
	height: 100%;
	background:#f1f1f1;
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	margin: auto;
}
.top{
	width: 100%;
	height:2.56rem;
	background:#ff7d40;
	display: flex;
	flex-direction: column;
}
.top-right{
	display: flex;
	justify-content: flex-end;
	align-items: center;
	height:0.8rem;
}
.top-right img{
	width: 0.42rem;
	height: 0.46rem;
	margin-right:0.2rem;
}
.top-left{
	height:1.2rem;
	display: flex;
	justify-content: flex-start;
	align-items: center;
}
.top-head{
	width: 1.2rem;
	height: 1.2rem;
	border-radius: 50%;
	margin:0 0.4rem;
}
.top-head img{
	width: 100%;
	height: 100%;
}
.top-login{
	color: #fff;
	font-size:0.4rem;
}
.my_order{
	height: 0.9rem;
	background: #fff;
	padding: 0 0.5rem;
	line-height: 0.9rem;
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom:0.3rem;
	font-size:0.28rem;
}
.my_order .my_allorder{
	background: url("../../assets/my/arr_right_small.png") no-repeat right center;
	width:1.4rem;
	color: #999;
}
.goodsStatus{
	height: 1.68rem;
	background: #fff;
	margin-bottom: 0.3rem;
}
</style>