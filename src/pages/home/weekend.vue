<template>
	<div>
		<h3>周末去哪儿</h3>
		<ul>
			<li v-for="item of weekendlist" :key="item.id">
				<a href="">
					<div class="imgage">
						<img :src="item.src" alt="">
					</div>
					<div class="text">
						<p>{{item.title}}</p>
						<p>{{item.introduce}}</p>
					</div>
				</a>
			</li>
		</ul>
	</div>
</template>

<script>
	export default{
		data(){
			return {
				
			}
		},
		props:["weekendlist"]
	}
</script>


<style scoped>
h3{
	font-weight: 400;
	font-size: 1.6rem;
	text-align: left;
	line-height: 1.8rem;
	padding: 1.2rem;
}
a{
	text-decoration: none;
	color: inherit;
	display: block;
	overflow: hidden;
	width: 100%;
	background-color: #fff;
	margin-bottom: .8rem;
}
.imgage img{
	width: 100%;
}
.text{
	text-align: left;
	padding: 1rem;
}
p{
	font-size: 1.6rem;
	line-height: 2rem;
}
.text p:last-child{
	font-size: 1.2rem;
	overflow: hidden;
	white-space: nowrap;
	text-overflow: ellipsis;
}
</style>