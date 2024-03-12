<template>
	<view class="sortBox">
		<view class="boxTop">
			<view class="sort-search">
				<view class="sort-search-left">
					花仙子
				</view>
				<view class="sort-search-right">
					<view class="sort-search-right-image">
						<uni-icons color="#999999" size="26" type="search" />
					</view>
				</view>
			</view>
			<Collect class="sort-collect"></Collect>
			<view class="sort-broadcast">
				<view style="color: #ffbcc5;margin-right: 6px;">花</view>
				<view style="color: #41414d">播&nbsp;报</view>
				<view style="margin: 0 6px;font-weight: normal;">|</view>
				<view style="font-weight: normal;font-size: 14px;">本店支持优惠券</view>
			</view>
			<view class="sort-type">
				<view class="sort-type-item" @click="pickTypeEvt(1)">
					<img :class="typeValue==1?'':'opcity'" class="sort-type-item-img" src="static/state.png" alt="">
					<view class="sort-type-item-text" :class="typeValue==1?'sort-type-item-text-checked':''">
						经典样式
					</view>
				</view>
				<view class="sort-type-item" @click="pickTypeEvt(2)">
					<img :class="typeValue==2?'':'opcity'" class="sort-type-item-img" src="static/state.png" alt="">
					<view class="sort-type-item-text" :class="typeValue==2?'sort-type-item-text-checked':''">
						人气推荐
					</view>
				</view>
			</view>
		</view>
		<view class="sortBox-scoll">
			<Popularity v-show="typeValue==2"></Popularity>
			<Classics v-show="typeValue==1"></Classics>
		</view>
		
	</view>
	
</template>

<script>
	import uniIcons from '../../components/uni-icons/uni-icons.vue';
	import Collect from './component/Collect.vue';
	import Popularity from './component/Popularity.vue';
	import Classics from './component/Classics.vue';
	export default{
		name:'Sort',
		components:{
			uniIcons,
			Collect,
			Popularity,
			Classics
		},
		data(){
			return{
				typeValue:1,
			}
			
		},
		methods:{
			pickTypeEvt(type){
				this.typeValue = type;
			}
		}
	}
</script>

<style>
	
	.sortBox{
		height: 100%;
		width: 100%;
		box-sizing: border-box;
		/* padding: 12px; */
		padding-bottom: 0;
		position: relative;
	}
	.boxTop{
		width: 100%;
		position: fixed;
		top: 44px;
		left: 0;
		height: 220px;
	}
	.sort-search{
		height: 50px;
		display: flex;
		justify-content: space-between;
		padding: 12px;
		padding-bottom: 0;
		box-sizing: border-box;
	}
	.sort-search-left{
		box-sizing: border-box;
		width: 100px;
		height: 38px;
		line-height: 38px;
		border-radius: 16px;
		border: 1px solid #f0f0f0;
		text-align: right;
		padding: 0 10px;
		background: url('../../static/ping.png') left center no-repeat;
		background-size: 45%;
	}
	.sort-search-right{
		width: 36px;
		height: 100%;
		margin-right: 80px;
		border: #f0f0f0 1px solid;
		border-radius: 19px;
		text-align: center;
		line-height: 36px;
	}
	.sort-collect{
		margin-top: 15px;

	}
	.sort-broadcast{
		width: 100%;
		height: 30px;
		background-color: #fff7fa;
		display: flex;
		font-size: 18px;
		line-height: 30px;
		padding: 0 10px;
		box-sizing: border-box;
		font-weight: bold;
		
	}
	.sort-type{
		display: flex;
		height: 60px;
		box-sizing: border-box;
		align-items: flex-end;
		justify-content: space-evenly;
		font-size: 16px;
		font-weight: bold;
		color: #909090;
	}
	.sort-type-item{
		display: flex;
		align-items: center;
		height: 40px;
	}
	.sort-type-item-img{
		height: 30px;
		margin-right: 6px;
	}
	.sort-type-item-text{
		height: 100%;
		line-height: 40px;
	}
	.sort-type-item-text-checked{
		border-bottom: #ff9092 3px solid;
		color: #41414d;
	}
	.opcity{
		opacity: 0;
	}
	.sortBox-scoll{
		position: absolute;
		top: 220px;
		left: 0;
		width: 100%;
		background-color: #f0f0f0;
		height: calc(100vh  - 314px);
		overflow-y: auto;
	}
	
</style>