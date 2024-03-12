<template>
	<!-- 收藏店铺 -->
	<view class="collectBox">
		<view class="collectBox-left">
			<view class="collectBox-left-top">
				<img class="collectBox-left-top-image" :src=collectPicture alt="收藏" @click='collectStoreEvt'>
				<view class="collectBox-left-top-bold">
					百合村店
				</view>
				<view class="collectBox-left-top-click">
					>
				</view>
			</view>
			<view class="collectBox-left-bottom">
				<view class="collectBox-left-bottom-grey">
					距离您
				</view>
				<view class="collectBox-left-bottom-num">
					0.3km
				</view>
			</view>
		</view>
		<view class="collectBox-right">
			<view :class="isChecked==1?'collectBox-right-item-checked':'collectBox-right-item'" @click="changeCkecked(1)">
				自取
			</view>
			<view :class="isChecked==2?'collectBox-right-item-checked':'collectBox-right-item'" @click="changeCkecked(2)">
				外卖
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				isChecked:1,
				collectPicture:'static/star.png',
				isCoolected:false,
			}
		},
		methods:{
			changeCkecked(type){
				if(type == 1){
					this.isChecked = 1;
				}else{
					this.isChecked = 2;
				}
			},
			collectStoreEvt(){
				this.isCoolected = !this.isCoolected;
				if(this.isCoolected){
					this.collectPicture='static/starChecked.png';
				}else{
					this.collectPicture='static/star.png';
				}
			}
			
		}
		
	}
</script>

<style>
	.collectBox{
		height: 60px;
		width: 100%;
		display: flex;
		justify-content: space-between;
		padding: 0 10px;
		box-sizing: border-box;
	}
	.collectBox-left{
		display: flex;
		flex-direction: column;
		height: 100%;
	}
	.collectBox-left-top{
		box-sizing: border-box;
		display: flex;
		height: 32px;
	}
	.collectBox-left-top-image{
		height: 100%;
		margin-right: 8px;
		cursor: pointer;
	}
	.collectBox-left-top-bold{
		font-weight: bold;
		font-size: 18px;
		line-height: 32px;
		color: #41414d;
	}
	.collectBox-left-top-click {
		margin-left: 10px;
		line-height: 32px;
		cursor: pointer;
	}
	.collectBox-left-bottom{
		box-sizing: border-box;
		height: 28px;
		display: flex;
		font-size: 14px;
	}
	.collectBox-left-bottom-grey{
		color: #d5d5d5;
		margin-right: 8px;
	}
	.collectBox-left-bottom-num{
		font-weight: bold;
	}
	.collectBox-right{
		width: 96px;
		height: 30px;
		background-color: #eeeeee;
		border: 1px solid #d5d5d5;
		border-radius: 6px;
		display: flex;
		padding: 2px;
		box-sizing: border-box;
		font-size: 12px;
		color: #fff;
		justify-content: space-between;
	}
	.collectBox-right-item{
		padding: 0 10px;
		border-radius: 6px;
		line-height: 25px;
		cursor: pointer;
		color: #bebebe;
	}
	.collectBox-right-item-checked{
		padding: 0 10px;
		background: linear-gradient(#ffbcc5,#ffd5ea);
		border-radius: 6px;
		line-height: 25px;
		color: #fff;
		cursor: pointer;
	}
</style>