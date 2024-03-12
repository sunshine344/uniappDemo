<template>
	<view class="userInfo">
		<!-- 用户头像 -->
		<view class="info-photo">
			<view class="photoImg">
				<img class="photoSize" src="static/photo.png" alt="头像">
			</view>
			<view class="photo-name">
				<view class="infoTop">
					<view style="font-size: 14px;font-weight: bold;">微信用户</view>
					<view class="infoTopRight">
						<img class="levelImg" src="static/level.png" alt="level">
						<view class="levelText">LV&nbsp;1</view>
					</view>
				</view>
				<view class="infoBottom">
				<text>距离</text>
				<text class="otherColor">V2</text>
				<text>还差</text>
				<text class="otherColor">10</text>
				<text>成长值</text>
				<text class="bottomClick" >></text>
			</view>
			</view>
			
		</view>
		<!-- 积分 -->
		<view class="info-integral">
			<view class="integral-top">我的积分 11</view>
			<view class="integral-bottom">
				<view class="integral-point"></view>
				<view class="integral-mall">积分商城&nbsp;></view>
			</view>
		</view>
	</view>
</template>

<script>
</script>

<style>
	.userInfo{
		background-color: #fff;
		height: 70px;
		border-radius: 10px;
		display: flex;
		width: 100%;
		box-sizing: border-box;
		padding: 0 12px;
		justify-content: space-between;
	}
	.info-photo{
		display: flex;
		align-items: center;
	}
	.photoImg{
		margin-right: 6px;
	}
	.photo-name{
		display: flex;
		flex-direction: column;
		font-size: 12px;
		height: 100%;
		justify-content: space-between;
		box-sizing: border-box;
		padding: 12px 0;

	}
	.infoTop{
		display: flex;
		align-items: flex-start;
		box-sizing: border-box;
	}
		
	.infoTopRight{
		position: relative;
		left: 10px;
	}
	.levelImg{
		width: 28px;
		height: 26px;
	}
	.levelText{
		position: absolute;
		color: #00aa7f;
		left: 50%;
		top: 50%;
		transform:translate(-50%,-50%) scale(0.8);
	}
	.photoSize{
		width: 45px;
		height: 45px;
	}
	.otherColor{
		color: #ff5500;
	}
	.bottomClick{
		margin-left: 8px;
		font-size: 16px;
		cursor: pointer;
		color: #7d7d7d;
	}
	.info-integral{
		font-size: 12px;
		padding: 12px 0;
	}
	.integral-top{
		font-size: 14px;
		font-weight: bold;
		margin-bottom: 8px;
	}
	.integral-bottom{
		display: flex;
		align-items: center;
	}
	.integral-point{
		width: 8px;
		height: 8px;
		background-color: red;
		border-radius: 4px;
		margin-right: 6px;
	}
	.integral-mall{
		cursor: pointer;
	}
</style>