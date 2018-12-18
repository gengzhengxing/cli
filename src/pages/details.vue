<template>
	<div>
		<a href="history.go(-1)" class="iconfont block3">&#xe74f;</a>
		<headdetail :title="detailslist.title"></headdetail>
		<imgHead :list="detailslist"></imgHead>
		<promoteArea :items="detailslist.product.recommend" v-if="detailslist.product.recommend"></promoteArea>
		<ticket :items="detailslist.product.ticket" titleType="门票" v-if="detailslist.product.ticket"></ticket>
		<ticket :items="detailslist.product.sale" titleType="促销" v-if="detailslist.product.sale"></ticket>
		<ticket :items="detailslist.product.ticketPackage" titleType="套票" v-if="detailslist.product.ticketPackage"></ticket>
		<ticket :items="detailslist.product.scenicService" titleType="景区服务" v-if="detailslist.product.scenicService"></ticket>
		<ticket :items="detailslist.product.dayTrip" titleType="一日游" v-if="detailslist.product.dayTrip"></ticket>
		<ticket :items="detailslist.product.hanyangling" titleType="汉阳陵" v-if="detailslist.product.hanyangling"></ticket>
		<ticket :items="detailslist.product.hylandtyg" titleType="汉阳陵和陶艺馆" v-if="detailslist.product.hylandtyg"></ticket>
		<ticket :items="detailslist.product.taoyiguan" titleType="陶艺馆" v-if="detailslist.product.taoyiguan"></ticket>
		<ticket :items="detailslist.product.weekendticket" titleType="周末门票" v-if="detailslist.product.weekendticket"></ticket>
		<ticket :items="detailslist.product.Eguide" titleType="电子讲解服务" v-if="detailslist.product.Eguide"></ticket>
		<ticket :items="detailslist.product.qinziticket" titleType="亲子票" v-if="detailslist.product.qinziticket"></ticket>
		<ticket :items="detailslist.product.activeticket" titleType="活动票" v-if="detailslist.product.activeticket"></ticket>
		<ticket :items="detailslist.product.zhinengnav" titleType="智能导航服务" v-if="detailslist.product.zhinengnav"></ticket>
		<ticket :items="detailslist.product.hotsale" titleType="热门促销" v-if="detailslist.product.hotsale"></ticket>
		<ticket :items="detailslist.product.shuangdan" titleType="双旦" v-if="detailslist.product.shuangdan"></ticket>
		<ticket :items="detailslist.product.chengrenticket" titleType="成人套票" v-if="detailslist.product.chengrenticket"></ticket>
		<ticket :items="detailslist.product.playfun" titleType="玩乐" v-if="detailslist.product.playfun"></ticket>
		<div class="remainder">
			<a href="#">
				查看剩余产品
				<span class="iconfont">&#xe783;</span>
			</a>
		</div>

		<commentArea :items="detailslist.comment" v-if="detailslist.comment"></commentArea>
		<!-- <ticket :items="detailslist.product.ticket" v-if="detailslist.product.ticket"></ticket> -->
		<!-- <list :items="detailslist"></list> -->
	</div>
</template>
<script>
	import headdetail from './details/headdetail'
	import imgHead from './details/imgHead'
	import promoteArea from './details/promoteArea'
	import ticket from './details/ticket'
	import commentArea from './details/commentArea'
	export default {
		data(){
			return {
				detailslist:{
					address: null,
					adv: null,
					bigImg: null,
					comment: null,
					count: null,
					detailsAddress: null,
					id: null,
					img: null,
					lab: null,
					labtit: null,
					price: null,
					product: {},
					score: null,
					title: null
				}
			}
		},
		components:{
			headdetail,
			imgHead,
			promoteArea,
			ticket,
			commentArea
		},
		mounted(){
			this.$axios.get("http://gengzhengxing.ltd/static/mock/detailsData.json").then((response)=>{
				this.detailslist = response.data[this.$route.query.id];
				// console.log(this.detailslist)
			})

		}
	}
</script>
<style>
	a.block3{
		position: absolute;
		z-index: 5;
		display: block;
		top: .4rem;
		left: .4rem;
		width: 3.6rem;
		height: 3.6rem;
		line-height: 3.6rem;
		color: #fff;
		font-size: 2.4rem;
		background-color: rgba(0, 0, 0, 0.4);
		border-radius: 100%;
	}
	.remainder{
		line-height: 3.2rem;
		background-color: #fff;
		border-top: 1px solid #f5f5f5;
		margin-bottom: 1rem;
	}
	.remainder a{
		display: block;
		text-align: center;
		color: #666;
		font-size: 1.4rem;
	}
</style>