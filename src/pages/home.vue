<template>
	<div>
		<headHome></headHome>
		<autoImgHome></autoImgHome>
		<navHome></navHome>
		<twoNavAndPosition></twoNavAndPosition>
		<advHome></advHome>
		<weekAllHot :hotlist="hotlist"></weekAllHot>
		<likeList :likelist="likelist"></likeList>
		<weekend :weekendlist="weekendlist"></weekend>
	</div>
</template>

<script>
	
	import headHome from './home/headHome'
	import autoImgHome from './home/autoImgHome'
	import navHome from './home/navHome'
	import twoNavAndPosition from './home/twoNavAndPosition'
	import advHome from './home/advHome'
	import weekAllHot from './home/weekAllHot'
	import likeList from './home/likeList'
	import weekend from './home/weekend'
	export default {
		data(){
			return {
				hotlist:null,
				likelist:null,
				weekendlist:null
			}
		},
		components:{
			headHome,
			autoImgHome,
			navHome,
			twoNavAndPosition,
			advHome,
			weekAllHot,
			likeList,
			weekend
		},
		mounted(){
			this.$axios.get("http://gengzhengxing.ltd/static/mock/homeData.json").then((response)=>{
				this.hotlist = response.data.hotlist;
				this.likelist = response.data.likelist;
				this.weekendlist = response.data.weekendlist;
			})
		}
	}
</script>