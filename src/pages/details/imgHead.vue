<template>
	<div>
		<div class="head2">
			
			<div>
				<img :src="list.bigImg" alt="">
			</div>
			<div class="zhezhao"></div>
			<div class="titleHead">
				{{list.title}}
			</div>
		</div>
		<div class="baseinfo">
			<div class="info">
				<div class="left">
					<div>
						<span class="commentscore">{{list.score}}</span>
						<span class="commenttext">分</span>
					</div>
					<div>
						<span class="commentnum">{{list.count}}条评论</span>
						<span class="iconfont rightarrow">&#xe70c;</span>
					</div>
				</div>
				<div class="right">
					<div>
						<span class="sighttitle">景点简介</span>
					</div>
					<div>
						<span class="sighttext">开放时间、贴士</span>
						<span class="iconfont rightarrow" style="right:0;">&#xe70c;</span>
					</div>
				</div>
			</div>
			<div class="defailsaddress">
				<p>
					<span class="iconfont addressicon">&#xe6f8;</span>
					<span class="detailsAddress">{{list.detailsAddress}}</span>
					<span class="iconfont addressarrow">&#xe70c;</span>
				</p>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		data(){
			return {

			}
		},
		props:["list"]
	}
</script>

<style scoped>
.head2{
	width: 100%;
	position: relative;
}
.zhezhao{
	position: absolute;
	bottom: 0;
	background: linear-gradient(to top,rgba(0, 0, 0, 0.8),rgba(255, 255, 255, 0));
	width: 100%;
	height: 5rem;
}
.head2 img{
	width: 100%;
}
.titleHead{
	margin-left: 1.6rem;
	position: absolute;
	bottom: 1.5rem;
	left: 0;
	color: #fff;
	font-size: 1.8rem;
}
.baseinfo{
	text-align: left;
	background-color: #fff;
	padding: .6rem .6rem 0 .6rem;
	border-top-left-radius: .4rem;
	border-top-right-radius: .4rem;
	position: relative;
	top: -.8rem;
	box-sizing: border-box;
}
.info{
	overflow: hidden;
	padding-top: .8rem;
}
.left,.right{
	float: left;
	width: 50%;
	box-sizing: border-box;
	position: relative;
}
.left{
	padding-left: 1rem;
	border-right: 1px solid #eee;
}
.left .commenttext{
	color: #ff8300;
}
.left .commentscore{
	color: #ff8300;
	font-size: 2.4rem;
	line-height: 1.4rem;
}
.right{
	padding-left: 1.5rem;
}
.rightarrow{
	position: absolute;
	right: 0;
	top: 50%;
	transform: translate(0, -50%);
}
.sighttitle{
	font-size: 1.4rem;
}
.left div:last-child,.right div:last-child{
	font-size: 1.2rem;
	color: #999;
	margin-top: .8rem;
}
.defailsaddress{
	margin-top: .8rem;
	line-height: 3.6rem;
	border-top: 1px solid #eee;
	font-size: 1.4rem;
	color: #333;
	position: relative;
	overflow: hidden;
}
.addressicon{
	float: left;
	margin: 0 .6rem;
	font-size: 2.4rem;
}
.addressarrow{
	position: absolute;
	right: .8rem;
}
.detailsAddress{
	float: left;
	width: 70%;
}
</style>