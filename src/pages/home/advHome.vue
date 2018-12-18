<template>
	<ul class="threenav">
		<li>
			
		</li>
		<li>
			
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
	.threenav{
		width: 100%;
		border-top: 1px solid #e0e0e0;
		font-size: 1.4rem;
		color: #212121;
		height: 5.2rem;
		margin-bottom: .6rem;
	}
	.threenav li{
		box-sizing: border-box;
		width: 50%;
		height: 5.2rem;
		line-height: 5.2rem;
		float: left;
	}
	.threenav li:first-child{
		border-right: 1px solid #e0e0e0;
		background: url('/static/images/adv1.png') no-repeat center #fff;
		background-size: contain;
	}
	.threenav li:last-child{
		background: url('/static/images/adv2.png') no-repeat center #fff;
		background-size: contain;
	}
</style>