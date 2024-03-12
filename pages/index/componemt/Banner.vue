<template>
	<swiper class="banner-box" autoplay="3000" circular >
		<swiper-item v-for="(item,index) in bannerList" :key="index">
			<view class="swiper-item"><img class="swiper-item-img" :src="item.path" alt="banner"></view>
		</swiper-item>
	</swiper>
</template>

<script>
	export default {
		components: {},
		data() {
			return {
				bannerList:[
					{id:1,path:'static/banner01.png'},
					{id:2,path:'static/banner02.png'},
					{id:3,path:'static/banner03.png'},
					{id:4,path:'static/banner04.png'},
					{id:5,path:'static/banner05.png'},
				],
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.banner-box{
		height: 280px;
	}
	.swiper-item-img{
		height:100%;
		width: 100%;
	}
</style>