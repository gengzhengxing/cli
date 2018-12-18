<template>
	<div class="box3">
		<h2>
			去哪儿推荐
		</h2>
		<ul>
			<li v-for="(item,index) in items" :key="index">
				<div class="left">
					<h3>{{item.name}}</h3>
					<div class="time">
						{{item.remark[0]}}
					</div>
					<div class="label">
						<span v-for="str of item.label">{{str}}</span>
					</div>
				</div>
				<div class="right">
					<a href="#">
						<div class="price">
							￥
							<em>{{item.price}}</em>
							<span>起</span>
						</div>
						<div class="mbtn">预定</div>
					</a>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		props:["items"]
	}
</script>

<style scoped>
	.box3 h2,.box3 h3{
		font-weight: 400;
	}
	.box3{
		text-align: left;
		padding-left: .8rem;
		background-color: #fff;
		padding-bottom: 1rem;
	}
	.box3 h2{
		font-size: 1.6rem;
		line-height: 3.6rem;
		padding-left: 2.4rem;
		background: url('/static/images/tuijian.png') no-repeat center left;
		background-size: 1.8rem 1.8rem;
		color: #333;
	}
	.box3 li{
		box-sizing: border-box;
		border-top: 1px solid #f5f5f5;
		padding-top: 1rem;
		margin-top: 1rem;
		position: relative;
	}
	.box3 li:first-child{
		margin-top: 0;
	}
	.box3 h3{
		font-size: 1.6rem;
		color: #333;
	}
	.box3 .left{
		width: 65%;
	}
	.box3 .time{
		margin: .3rem 0;
		padding-left: 1.2rem;
		background: url('/static/images/shijian.png') no-repeat center left;
		background-size: 1rem 1rem;
		color: #333;
	}
	.box3 .label span{
		font-size: 1rem;
		border-radius: .2rem;
		border: 1px solid #a5e4ec;
		margin: .2rem .2rem;
		color: #00afc7;
	}
	.box3 .right{
		position: absolute;
		right: 1.6rem;
		top: 50%;
		transform: translate(0, -30%);
	}
	.box3 .price{
		font-size: 1rem;
		color: #ff8300;
		text-align: center;
	}
	.box3 .price em{
		font-size: 2.0rem;
		font-style: normal;
	}
	.box3 .price span{
		color: #666;
		font-size: .8rem!important;
	}
	.box3 .mbtn{
		width: 8rem;
		line-height: 2.6rem;
		text-align: center;
		color: #fff;
		background-color: #ff8300;
		font-size: 1.5rem;
		border-radius: .2rem;
	}
</style>