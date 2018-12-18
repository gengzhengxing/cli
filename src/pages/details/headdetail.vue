<template>
	<header class="head1">
		<a class="iconfont block" href="/">&#xe74f;</a>
		<h1>{{title}}</h1>
	</header>
</template>

<script>
	export default {
		data(){
			return {

			}
		},
		props:["title"]
	}
</script>

<style scoped>
	header.head1{
		position: fixed;
		width: 100%;
		top: 0px;
		left: 0px;
		display: none;
		z-index: 2;
	}
	header.head1 a{
		position: absolute;
		left: 0;
		top: 0;
		width: 4rem;
		height: 4.4rem;
		line-height: 4.4rem;
		font-size: 2.4rem;
		color: #fff;
		text-align: center;
	}
	header.head1 h1{
		overflow: hidden;
		margin: 0 .5rem;
		line-height: 4.4rem;
		white-space: nowrap;
		text-overflow: ellipsis;
		font-size: 1.6rem;
		text-align: center;
		color: #fff;
		opacity: 0;
	}
</style>