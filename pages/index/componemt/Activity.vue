<template>
	<view class="activity">
		<view class="activity-item activity-item-img">
			<!-- <img class="activity-item-img" src="static/vip.png" alt="vip"> -->
		</view>
		<view class="activity-item">
			<view class="activity-item-gift">邀请有礼</view>
			<view class="activity-item-invite">邀请好友8折券</view>
			<img class="activity-item-image" src="../../../static/gift.png"/>
		</view>
		<view class="activity-item">
			<view class="activity-item-gift">鲜花日历</view>
			<view class="activity-item-invite">签到赢好礼</view>
			<img class="activity-item-image" src="../../../static/qian.png"/>
		</view>
	</view>
</template>

<script>
</script>

<style>
	.activity{
		display: flex;
		padding: 0 12px;
		align-items: center;
		justify-content: space-between;
		box-sizing: border-box;
		height: 84px;
	}
	.activity-item{
		height: 100%;
		background-color: #fff;
		width: 32%;
		border-radius: 8px;
		cursor: pointer;
		position: relative;
	}
	.activity-item-img{
		background-image: url('../../../static/vip.png');
		background-position: center;
		background-repeat: no-repeat;
		background-size: 100%;
	}
	.activity-item-gift{
		font-weight: bold;
		margin-top: 8px;
		margin-left: 12px;
	}
	.activity-item-invite{
		font-size: 12px;
		color: #a1a1a1;
		margin-left: 12px;
	}
	.activity-item-image{
		height: 55%;
		position: absolute;
		bottom: 0;
		right: 0;
	}
</style>