<template>
	<header>
		<i class="iconfont">&#xe74f;</i>
		<div class="search">
			<input type="text" placeholder="输入城市/景点/游玩主题"><i class="iconfont">&#xe77c;</i>
		</div>
		<span>
			{{city}}
			<em class="iconfont">&#xe783;</em>
		</span>
	</header>
</template>

<script>
	export default {
		data(){
			return {
				city:"咸阳"
			}
		}
	}
</script>

<style scoped>
	header{
		height: 4.4rem;
		line-height: 4.4rem;
		background-color: #00bcd4;
		font-size: 1.4rem;
		color: #fff;
		overflow: hidden;
	}
	header>i,header .search{
		float: left;
	}
	header>i{
		width: 10%;
	}
	header .search{
		width: 64%;
		height: 3.6rem;
		margin-top: .6rem;
		position: relative;
	}
	header .search i{
		padding-left: 1rem;
	    width: 2rem;
	    line-height: 3.4rem;
	    color: #e4e7ea;
	    font-size: 2rem;
	    position: absolute;
	    top: 0;
	    left: 0;
	}
	header .search input{
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		outline: none;
		border: none;
		border-radius: 4px;
		padding-left: 3rem;
		height: 3.2rem;
	}
	header .search input::placeholder{
		color: #e4e7ea;
	}
	header span{
		float: right;
		width: 17%;
	}
</style>