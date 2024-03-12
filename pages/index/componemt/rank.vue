<template>
	<view class="rankBox">
		<view class="rank">
			<view class="rank-item" v-for="it in itemList" :key="it.id">
				<view class="rank-item-top">
					<view class="rank-item-top-red">Top{{it.id}}</view>
				</view>
				<view class="rank-item-image">
					<img class="rank-item-image-size" :src="it.img" alt="商品">
				</view>
				<view class="rank-item-info">
					<view class="rank-item-info-name">{{it.name}}</view>
					<view class="rank-item-info-sold">昨天已售卖{{it.num}}束</view>
					<view class="rank-item-info-add">＋</view>
				</view>
			</view>
		</view>
		
		<view class="bottom-line">这已经是我的底线了~</view>
	</view>
	
	
</template>

<script>
	export default {
		components: {},
		data() {
			return {
				itemList:[
					{id:1,name:'郁金香',num:283,img:'static/hua1.png'},
					{id:2,name:'香槟玫瑰',num:234,img:'static/hua2.png'},
					{id:3,name:'洋吉梗',num:212,img:'static/hua3.png'},
					{id:4,name:'绿色玫瑰',num:186,img:'static/hua4.png'},
					{id:5,name:'白色郁金香',num:177,img:'static/hua5.png'},
					{id:6,name:'红玫瑰',num:152,img:'static/hua6.png'},
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.rank{
		margin: 20px 12px;
		display: flex;
		box-sizing: border-box;
		justify-content: space-between;
		flex-wrap: wrap;
	}
	.rank-item{
		width: 49%;
		border-radius: 8px;
		box-sizing: border-box;
		background-color: #fff;
		height: 240px;
		margin-bottom: 10px;
		
	}
	.rank-item-top{
		height: 16%;
		position: relative;
	}
	.rank-item-top-red{
		background-color: #ff6565;
		height:24px;
		width: 48px;
		position: absolute;
		top: 0;
		right: 0;
		border-radius: 0 8px 0 8px;
		text-align: center;
		line-height: 24px;
		color: #fff;

	}
	.rank-item-image{
		background-color: #fcfcfc;
		height: 50%;
		text-align: center;
	}
	.rank-item-image-size{
		height: 100%;
	}
	.rank-item-info{
		padding: 10px;
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		justify-content: space-around;
		height: 34%;
		position: relative;
		align-items: flex-start;
	}
	.rank-item-info-sold{
		color: #7d7d7d;
		transform: scale(0.8);
	}
	.rank-item-info-add{
		width: 24px;
		height: 24px;
		border-radius: 12px;
		background-image: radial-gradient(#b8a6ff,#b390ff);
		color: #fff;
		text-align: center;
		line-height: 24px;
		position: absolute;
		right: 12px;
		bottom: 12px;
		font-weight: bold;
		font-size: 20px;
	}
	.bottom-line{
		text-align: center;
		color: #7d7d7d;
		font-size: 12px;
	}
</style>