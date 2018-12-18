<template>
	<div class="weekhot">
		<div class="top1">
			<img class="hotimg" src="@/assets/images/hot.png" alt="">
			<span>本周热门榜单</span>
			<a href="#">
				全部榜单
				<i class="iconfont">&#xe70c;</i>
			</a>
		</div>
		<ul>
			<li v-for="item of hotlist" :key="item.id">
				<router-link :to="{path:'/details',query:{id:item.id}}" class="block">
					<div class="lab">
						<img :src="item.lab">
					</div>
					<div><img :src="item.img"></div>
					<div class="scenic">{{item.site}}</div>
					<div>
						<span class="sign">￥{{item.price}}</span>起
					</div>
				</router-link>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		data(){
			return {
				
			}
		},
		props:["hotlist"]
	}
</script>





<style scoped>
	.weekhot{
		background: #fff;
		margin-bottom: .8rem;
	}
	.top1{
		position: relative;
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
	.top1 span{
		height: 2.2rem;
		line-height: 2.2rem;
		font-size: 1.6rem;
		color: #212121;
		margin-left: 0.4rem;
	}
	.top1 a{
		position: absolute;
		top: 1.8rem;
		right: 1.6rem;
		color: #616161;
		font-size: 1.4rem;
		line-height: 1.4rem;
		text-decoration: none;
	}
	.weekhot ul{
		display: flex;
		padding: 1.2rem;
		overflow-x: scroll;
		white-space: nowrap;
	}
	.weekhot li{
		float: left;
		width: 8.34rem;
		margin-right: 1rem;
		position: relative;
	}
	.weekhot li .block{
		font-size: 1.2rem;
		color: inherit;
		text-decoration: none;
	}
	.weekhot li img{
		width: 8.34rem;
		display: block;
	}
	.lab{
		position: absolute;
		top: 0;
		left: 0;
		z-index: 1;
		overflow: hidden;
		width: 4.2rem;
		height: 2rem;
	}
	.weekhot li .lab img{
		width: 100%;
	}
	.scenic{
		margin-top: 0.6rem;
		color: #212121;
		font-size: 1.2rem;
		line-height: 1.6rem;
		text-align: center;
		overflow: hidden;
		width: 100%;
		white-space: nowrap;
		text-overflow: ellipsis;
	}
	.sign{
		color: #ff8300;
	}
</style>