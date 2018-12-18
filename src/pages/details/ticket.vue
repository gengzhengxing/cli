<template>
	<div class="box4">
		<h3>
			{{titleType}}
		</h3>
		<div class="ticket" v-for="item of items">
			<h5>{{item.name}}</h5>
			<div class="price">
				￥
				<em>{{item.price}}</em>
				<span>起</span>
			</div>
			<div class="iconfont bottomarrow">&#xe783;</div>
		</div>
	</div>
</template>

<script>
	export default {
		props:["items","titleType"]
	}
</script>

<style scoped>
	.box4{
		margin-top: .8rem;
		background-color: #fff;
	}
	.box4 h3,.box4 h5{
		font-weight: 400;
		text-align: left;
	}
	.box4 em{
		font-style: normal;
	}
	.box4 .ticket{
		position: relative;
		padding: 1.2rem 1rem;
		font-size: 1.4rem;
		border-bottom: 1px solid #f5f5f5;
	}
	.box4 .ticket:last-child{
		border-bottom: none;
	}
	.box4 h3{
		margin-left: .8rem;
		padding-left: 2.4rem;
		line-height: 3.2rem;
		font-size: 1.6rem;
		color: #333;
		border-bottom: 1px solid #f5f5f5;
		background: url('/static/images/detail.png') no-repeat center left;
		background-size: 2.2rem;
		background-position: 0 -1.8rem;
	}
	.box4 .price,.box4 .bottomarrow{
		position: absolute;
		top: 50%;
		transform: translate(0, -50%);
	}
	.box4 .ticket h5{
		font-size: 1.4rem;
		color: #333;
	}
	.box4 .price{
		right: 2.4rem;
		color: #ff8300;
	}
	.box4 .price em{
		font-size: 2.2rem;
	}
	.box4 .price span{
		color: #666;
		font-size: 1.2rem;
	}
	.box4 .bottomarrow{
		right: .8rem;
		color: #666;
		font-size: 1.8rem;
	}
</style>