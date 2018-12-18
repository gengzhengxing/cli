<template>
	<ul class="twonav">
		<li>
			<i class="iconfont">&#xe6f9;</i>
			定位失败
		</li>
		<li>
			<i class="iconfont">&#xe6f4;</i>
			必游榜单
		</li>
	</ul>
</template>

<script>
	export default {
		data(){
			return {

			}
		}
	}
</script>

<style scoped>
	.twonav{
		width: 100%;
		line-height: 4.6rem;
		border-top: 1px solid #e0e0e0;
		font-size: 1.4rem;
		color: #212121;
		background-color: #fff;
		margin-bottom: .6rem;
		overflow: hidden;
	}
	.twonav li{
		box-sizing: border-box;
		width: 50%;
		float: left;
	}
	.twonav li:first-child{
		border-right: 1px solid #e0e0e0;
	}
	.twonav li i{
		font-size: 1.8rem;
	}
</style>