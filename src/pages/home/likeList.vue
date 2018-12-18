<template>
	<div class="detaillike">
		<div class="top">
			<img class="hotimg" src="@/assets/images/love.png" alt="">
			<span>猜你喜欢</span>
		</div>
		<ol>
			<li v-for="item of likelist" :key="item.id">
				<router-link :to="{path:'/details',query:{id:item.id}}" class="block1">
					<div class="left">
						<img :src="item.img">
					</div>
					<div class="titcon" :style="{background:'url(' + item.lab + ')'}">
						{{item.labtit}}
					</div>
					<div class="right">
						<div class="title">
							{{item.title}}
						</div>
						<div class="score">
							<span class="star">
								<em :style="{width:(item.score/5*100 + '%')}" class="iconfont">&#xe6f4;&#xe6f4;&#xe6f4;&#xe6f4;&#xe6f4;</em>
								<strong class="iconfont">&#xe6f4;&#xe6f4;&#xe6f4;&#xe6f4;&#xe6f4;</strong>
							</span>
							<span class="count">
								<i>{{item.count}}</i>条评论
							</span>
						</div>
						<div class="pricecount">
							<span class="price">￥<em>{{item.price}}</em></span>
							起
							<span class="address">{{item.address}}</span>
						</div>
						<div class="bottom" v-show="!item.adv==''">{{item.adv}}</div>
					</div>
				</router-link>
			</li>
		</ol>
		<a href="#" class="all">查看所有产品</a>
	</div>
</template>

<script>
	export default {
		data(){
			return {
				
			}
		},
		props:["likelist"]
	}
</script>

<style scoped>
	.detaillike{
		background-color: #fff;
	}
	.top{
		padding: 1.2rem 1.4rem;
		text-align: left;
	}
	.hotimg{
		width: 1.5rem;
		height: 1.5rem;
		margin-left: 1rem;
		vertical-align: top;
		overflow: hidden;
	}
	.top span{
		height: 2.2rem;
		line-height: 2.2rem;
		font-size: 1.6rem;
		color: #212121;
		margin-left: 0.4rem;
	}
	ol{
		margin-left: 1.2rem;
	}
	ol li{
		position: relative;
		overflow: hidden;
		padding: 1rem 0;
		border-bottom: 1px solid #e0e0e0;
	}
	ol li:last-child{
		border-bottom: none;
	}
	.block1{
		display: block;
		text-decoration: none;
		color: inherit;
		width: 100%;
		height: 100%;
	}
	.block1 .left,.block1 .right{
		float: left;
	}
	.block1 .left{
		overflow: hidden;
		width: 8.34rem;
		height: 8.34rem;
	}
	.block1 .left img{
		width: 100%;
	}
	.block1 .right{
		box-sizing: border-box;
		text-align: left;
		padding-left: 1rem;
	}
	.block1 .title{
		margin-top: 1.3rem;
		height: 2.2rem;
		color: #212121;
		font-size: 1.6rem;
		line-height: 2.2rem;
		overflow: hidden;
		width: 100%;
		white-space: nowrap;
		text-overflow: ellipsis;
	}
	.block1 .score{
		margin-top: 0.7rem;
		height: 1.7rem;
	}
	.star{
		display: inline-block;
		position: relative;
		width: 7.5rem;
		height: 1.4rem;
		line-height: 1.4rem;
		font-size: 1.4rem;
		letter-spacing: 0.2rem;
		transform: scale(.83);
		transform-origin: 0 0;
	}
	.star em,.star strong{
		overflow: hidden;
		position: absolute;
		top: .2rem;
		left: 0;
		height: 1.4rem;
		font-size: 1.4rem;
		letter-spacing: 0;
		font-style: normal;
	}
	.star em{
		z-index: 2;
		color: #ffb436;
	}
	.star strong{
		z-index: 1;
		color: #e0e0e0;
	}
	.count{
		color: #616161;
		font-size: 1.2rem;
		line-height: 1.7rem;
		vertical-align: text-bottom;
	}
	.count i{
		font-style: normal;
	}
	.titcon{
		color: #fff;
		width: 5rem;
		line-height: 1.4rem;
		position: absolute;
		top: 1rem;
		left: 0;
		border-bottom-right-radius: .5rem;
		font-size: 1.2rem;
	}
	.pricecount{
		margin-top: 1.1rem;
		color: #616161;
		font-size: 1.2rem;
		line-height: 2rem;
	}
	.price{
		color: #ff8300;
	}
	.price em{
		font-style: normal;
		font-size: 2rem;
	}
	.address{
		position: absolute;
		right: 1.2rem;
	}
	.bottom{
		margin-top: 2.4rem;
		background: #fff9f9;
		padding: .2rem .5rem;
		color: #f55;
		font-size: 1.2rem;
		line-height: 1.7rem;
	}
	.detaillike a.all{
		display: block;
		width: 100%;
		font-size: 1.6rem;
		text-align: center;
		line-height: 4rem;
		color: #00afc7;
		border-top: 1px solid #e0e0e0;
	}
</style>