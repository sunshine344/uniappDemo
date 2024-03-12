<template>
	<view class="user">
		<view class="user-img"></view>
		<UserData class="user-data"></UserData>
	</view>
	
</template>

<script>
	import UserData from './components/UserData.vue';
	export default {
		components:{
			UserData,
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
	.user{
		width: 100%;
	}
	.user-img{
		width: 100%;
		height: 240px;
		background: url('../../static/banner03.png') no-repeat center center;
	}
	.user-data{
		height: 210px;
		width: calc(100% - 30px);
		padding: 0 20px;
		box-sizing: border-box;
		margin-top: -50px;
		text-align: center;
		margin-left: 15px;
	}
</style>