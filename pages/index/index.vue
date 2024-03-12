<template>
	<view class="container">
		<Banner class="container-banner" />
		<UserInfo class="containerInfo" />
		<SelectMode />
		<Activity class="con-activity"></Activity>
		<view class="con-guess">
			<view class="con-guess-title">
				<img class="con-guess-title-img" src="static/trophy.png" alt="">
				<view class="con-guess-title-text">猜你喜欢</view>
			</view>
			<view class="con-guess-gray">猜你所想的，懂你想要的</view>
		</view>
		<Rank />
	</view>
		
</template>

<script>
	import Banner from './componemt/Banner.vue';
	import UserInfo from './componemt/UserInfo.vue';
	import SelectMode from './componemt/SelectMode.vue';
	import Activity from './componemt/Activity.vue';
	import Rank from './componemt/rank.vue';
	export default {
		components:{
			Banner,
			UserInfo,
			SelectMode,
			Activity,
			Rank,
		},
		data() {
			return {
			}
		},
		methods: {

		},
	}
</script>

<style>
	.container {
		box-sizing: border-box;
		font-size: 14px;
		background-color:#f5f5f5;
		height: 100%;
		overflow-y: auto;
		position: relative;
	}
	.container-banner{
		height: 280px;
	}
	.containerInfo{
		position: absolute;
		left: 0;
		top: 250px;
		z-index: 99;
		width: calc(100% - 24px);
		margin: 0 12px;
	}
	.con-guess{
		margin-left: 18px;
		color: #9191E2;
		font-size: 22px;
		font-weight: bold;
		margin-top: 12px;
	}
	.con-guess-title{
		display: flex;
		align-items: center;
	}
	.con-guess-title-img{
		width: 7%;
	}
	.con-guess-gray{
		color: #a1a1a1;
		font-size: 14px;
	}
	
	
</style>
