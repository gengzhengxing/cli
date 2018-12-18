<template>
	<div class="box1">
		<h2>
			<span></span>
			用户评论
		</h2>
		<div class="comment" v-for="item of items">
			<div class="top">
				<span class="score">
					<em :style="{width:(item.score/5*100 + '%')}" class="iconfont">&#xe6f4;&#xe6f4;&#xe6f4;&#xe6f4;&#xe6f4;</em>
					<strong class="iconfont">&#xe6f4;&#xe6f4;&#xe6f4;&#xe6f4;&#xe6f4;</strong>
				</span>
				<span class="time">{{item.time}}</span>
				<span class="username">{{item.username}}</span>
			</div>
			<p>
				{{item.text}}
			</p>
			<span class="iconfont botarrow" v-if="item.text.length>120">&#xe783;</span>
			<ul class="bot" v-if="item.imgList">
				<li v-for="str of item.imgList">
					<img :src="str" alt="">
				</li>
				<div style="clear: both;"></div>
			</ul>
			
		</div>
		<div class="allcomment">
			查看全部评论
			<span class="iconfont">&#xe70c;</span>
		</div>
	</div>
</template>

<script>
	export default {
		props:["items"]
	}
</script>

<style scoped>
	.box1{
		text-align: left;
		background-color: #fff;
	}
	h2{
		font-size: 1.4rem;
		font-weight: 400;
		color: #666;
		line-height: 3.2rem;
	}
	h2 span{
		display: inline-block;
		width: .3rem;
		height: 1rem;
		background-color: #1ba9ba;
		margin: 0 .8rem;
	}
	.comment{
		border-top: 1px solid #f5f5f5;
		padding: 1rem;
	}
	.comment p{
		max-height: 105px;
		overflow: hidden;
		font-size: 1.4rem;
		color: #616161;
		line-height: 1.8rem;
		word-break:break-all;
		word-wrap: break-word;
	}
	.top{
		width: 100%;
	}
	.score{
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
	.score em,.score strong{
		overflow: hidden;
		position: absolute;
		top: .2rem;
		left: 0;
		height: 1.4rem;
		font-size: 1.8rem;
		letter-spacing: 0;
		font-style: normal;
	}
	.score em{
		z-index: 2;
		color: #ffb436;
	}
	.score strong{
		z-index: 1;
		color: #e0e0e0;
	}
	.time,.username{
		float: right;
		margin-right: .8rem;
		color: #666;
	}
	.botarrow{
		display: block;
		text-align: center;
		line-height: 3.2rem;
		color: #666;
		font-size: 2.4rem;
	}
	li img{
		width: 100%;
	}
	.bot{
		margin-top: 1.4rem;
	}
	.bot li{
		float: left;
		width: 30%;
		margin-right: .8rem;
	}
	.bot li:nth-child(3n){
		margin-right: 0;
	}
	.allcomment{
		border: 1px dashed #f5f5f5;
		text-align: center;
		line-height: 3.2rem;
		color: #666;
		font-size: 1.4rem;
	}
	.allcomment span{
		margin-left: 1.4rem;
	}
</style>