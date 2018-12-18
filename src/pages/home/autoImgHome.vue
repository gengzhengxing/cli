<template>
	<swiper :options="swiperOption" style="width:100%;">
		<!-- slides -->
		<swiper-slide v-for="(item,index) of imgList" :key="index">
			<img :src="item.src">
		</swiper-slide>
		<!-- Optional controls -->
		<div class="swiper-pagination"  slot="pagination"></div>
	</swiper>
</template>

<script>
	export default {
		data(){
			return {
				swiperOption:{
					loop:true,
					pagination: {
						el:'.swiper-pagination',
					}
				},
				imgList:[
					{
						src:require("@/assets/images/1.jpg")
					},
					{
						src:require("@/assets/images/2.jpg")
					},
					{
						src:require("@/assets/images/3.jpg")
					},
					{
						src:require("@/assets/images/4.jpg")
					},
					{
						src:require("@/assets/images/5.jpg")
					},
					{
						src:require("@/assets/images/6.jpg")
					},
					{
						src:require("@/assets/images/7.jpg")
					},
					{
						src:require("@/assets/images/8.jpg")
					},
					{
						src:require("@/assets/images/9.jpg")
					}
				]
			}
		}
	}
</script>

<style scoped>
	img{
		width: 100%;
		display: block;
	}
</style>