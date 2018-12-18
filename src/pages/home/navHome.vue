<template>
		<nav>
			<ul>
				<li v-for="(item,index) of navs" :key="index">
					<a href="#">
						<img :src="item.src" alt="">
						<p>{{item.title}}</p>
					</a>
				</li>
			</ul>
		</nav>
</template>

<script>
	export default {
		data(){
			return {
				navs:[
					{
						src:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						title:"景点门票"
					},
					{
						src:'http://img1.qunarzz.com/piao/fusion/1811/f6/e54fad3ea337b02.gif',
						title:"立减30"
					},
					{
						src:'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
						title:"游乐场"
					},
					{
						src:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
						title:"咸阳必游"
					},
					{
						src:'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
						title:"全部玩乐"
					}
				]
			}
		}
	}
</script>

<style scoped>
	nav{
		padding: .8rem 0;
		background-color: #fff;
	}
	nav ul{
		overflow: hidden;
	}
	nav li{
		width: 25%;
		float: left;
		margin-top: .4rem;
	}
	nav li img{
		width: 4.6rem;
	}
	nav li p{
		margin-top: .1rem;
		color: #212121;
		font-size: 1.4rem;
	}
	nav a{
		display: block;
		color: inherit;
		text-decoration: none;
	}
</style>