<template>
	<view class="way">
		<view class="way-item">
			<view class="item-text">到店取花</view>
			<img class="item-img" src="static/store.png" alt="到店取餐">
		</view>
		<view class="way-item">
			<view class="item-text">外卖到家</view>
			<img class="item-img" src="static/takeaway.png" alt="外卖到家">
		</view>
	</view>
</template>

<script>
</script>

<style>
	.way{
		height: 160px;
		margin: 50px 12px 12px 12px;
		box-sizing: border-box;
		display: flex;
		
	}
	.way-item{
		height: 100%;
		background-color: #fff;
		width: 50%;
		border-radius: 10px;
		text-align: center;
		box-sizing: border-box;
		padding: 12px 0;
		font-size: 18px;
		font-weight: 600;
		color: #6c6c6c;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
	}
	.item-img{
		width: 65%;
	}
	
</style>