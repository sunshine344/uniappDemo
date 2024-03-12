<template>
	<view class="classicsBox">
		<scroll-view class="classics-left" scroll-y="true" scroll-with-animation :scroll-into-view="clickId">
			<view v-for="(item,index) in contentData" :key="item.id" :id="item.id" class="classics-left-item" :class="picked==index?'checkedStyle':''" @click="selectActiveEvt(item)">
				{{item.title}}
			</view>
		</scroll-view>
		<!-- :scroll-top="scrollRightTop" -->
		<scroll-view scroll-y="true"  :scroll-into-view="clickId" :scroll-anchoring="true" scroll-with-animation class="classics-right" @scroll="scrollEvt">
			<view class="classics-right-item" v-for="item in contentData" :key="item.id" :id="item.id">
				<view class="title">
					{{item.title}}
				</view>
				<view class="item-box" v-for="it in item.content">
					<img class="item-box-left" :src="it.img" alt="">
					<view class="item-box-right">
						<view class="item-box-right-name">
							{{it.name}}
						</view>
						<view class="item-box-right-describe">
							{{it.desc}}
						</view>
						<view class="item-box-right-buy">
							<view class="item-box-right-price">
								￥{{it.price}}
							</view>
							<view class="item-box-right-pick">
								选规格
							</view>
						</view>
					</view>
				</view>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		components: {},
		data() {
			return {
				contentData:[
					{
						id:'tab1',
						title:'热销专区',
						content:[
							{id:101,img:'static/rexiao1.png',name:'郁金香',desc:'花语',price:'99',},
							{id:102,img:'static/rexiao2.png',name:'郁金香',desc:'花语',price:'99',},
							{id:103,img:'static/rexiao3.png',name:'郁金香',desc:'花语',price:'99',},
							{id:104,img:'static/rexiao4.png',name:'郁金香',desc:'花语',price:'99',},
							{id:105,img:'static/rexiao5.png',name:'郁金香',desc:'花语',price:'99',},
						]
					},
					{
						id:'tab2',
						title:'生日鲜花',
						content:[
							{id:201,img:'static/shengri1.png',name:'郁金香',desc:'花语',price:'99',},
							{id:202,img:'static/shengri2.png',name:'郁金香',desc:'花语',price:'99',},
							{id:203,img:'static/shengri3.png',name:'郁金香',desc:'花语',price:'99',},
							{id:204,img:'static/shengri4.png',name:'郁金香',desc:'花语',price:'99',},
							{id:205,img:'static/shengri5.png',name:'郁金香',desc:'花语',price:'99',},
						]
					},
					{
						id:'tab3',
						title:'浪漫玫瑰',
						content:[
							{id:201,img:'static/meigui7.png',name:'郁金香',desc:'花语',price:'99',},
							{id:202,img:'static/meigui2.png',name:'郁金香',desc:'花语',price:'99',},
							{id:203,img:'static/meigui3.png',name:'郁金香',desc:'花语',price:'99',},
							{id:204,img:'static/meigui4.png',name:'郁金香',desc:'花语',price:'99',},
							{id:205,img:'static/meigui5.png',name:'郁金香',desc:'花语',price:'99',},
							{id:205,img:'static/meigui6.png',name:'郁金香',desc:'花语',price:'99',},
							{id:205,img:'static/meigui1.png',name:'郁金香',desc:'花语',price:'99',},
						]
					},
					{
						id:'tab4',
						title:'郁金香区',
						content:[
							{id:201,img:'static/yjx1.png',name:'郁金香',desc:'花语',price:'99',},
							{id:202,img:'static/yjx2.png',name:'郁金香',desc:'花语',price:'99',},
							{id:203,img:'static/yjx6.png',name:'郁金香',desc:'花语',price:'99',},
							{id:204,img:'static/yjx4.png',name:'郁金香',desc:'花语',price:'99',},
							{id:205,img:'static/yjx5.png',name:'郁金香',desc:'花语',price:'99',},
						]
					},
					{
						id:'tab5',
						title:'表白祝福',
						content:[
							{id:201,img:'static/biaobai1.png',name:'郁金香',desc:'花语',price:'99',},
							{id:202,img:'static/biaobai2.png',name:'郁金香',desc:'花语',price:'99',},
							{id:203,img:'static/biaobai3.png',name:'郁金香',desc:'花语',price:'99',},
							{id:204,img:'static/biaobai4.png',name:'郁金香',desc:'花语',price:'99',},
							{id:205,img:'static/biaobai5.png',name:'郁金香',desc:'花语',price:'99',},
						]
					},
					{
						id:'tab6',
						title:'女士花束',
						content:[
							{id:201,img:'static/ns4.png',name:'郁金香',desc:'花语',price:'99',},
							{id:202,img:'static/ns2.png',name:'郁金香',desc:'花语',price:'99',},
							{id:203,img:'static/ns3.png',name:'郁金香',desc:'花语',price:'99',},
							{id:204,img:'static/ns1.png',name:'郁金香',desc:'花语',price:'99',},
						]
					},
					{
						id:'tab7',
						title:'草莓水果',
						content:[
							{id:201,img:'static/shuiguo1.png',name:'郁金香',desc:'花语',price:'99',},
							{id:202,img:'static/shuiguo2.png',name:'郁金香',desc:'花语',price:'99',},
							{id:203,img:'static/shuiguo3.png',name:'郁金香',desc:'花语',price:'99',},
							{id:204,img:'static/shuiguo4.png',name:'郁金香',desc:'花语',price:'99',},
							{id:205,img:'static/shuiguo5.png',name:'郁金香',desc:'花语',price:'99',},
							{id:205,img:'static/shuiguo6.png',name:'郁金香',desc:'花语',price:'99',},
						]
					},
					{
						id:'tab8',
						title:'小香风区',
						content:[
							{id:201,img:'static/xxf1.png',name:'郁金香',desc:'花语',price:'99',},
							{id:202,img:'static/xxf2.png',name:'郁金香',desc:'花语',price:'99',},
							{id:203,img:'static/xxf3.png',name:'郁金香',desc:'花语',price:'99',},
							{id:204,img:'static/xxf4.png',name:'郁金香',desc:'花语',price:'99',},
						]
					},
				],
				clickId:'tab1', //点击选项的id
				picked:0, // 左侧选中选项的index
				nowRightIndex:0, // 右边当前滚动的index
				itemArr:[], //用于存放右侧item位置数据
				scrollRightTop:0,
				timer:null,
			}
		},
		
		methods: {
			// 左侧切换点击事件
			selectActiveEvt(e) {
				this.clickId = e.id;
				this.picked = this.contentData.findIndex(it=>it.id==e.id);
			},
			scrollEvt(e){
				// 防抖
				if(this.timer){
					clearTimeout(this.timer);
				}
				this.timer = setTimeout(()=>{
					this.nowRightIndex =  this.itemArr.findLastIndex(it=>e.detail.scrollTop>=(it.bottom-228))+1; //判断当前顶部是处于哪个item，获取当前item的index
					if(this.nowRightIndex==-1) this.nowRightIndex=0;
					if(this.nowRightIndex==this.picked) return;
					this.clickId = this.contentData[this.nowRightIndex].id;
					this.picked = this.nowRightIndex;
				},500);
			},
			// 计算右侧每个item到顶部的距离，存放到数组
			getItemDistence(){
				new Promise(resolve=>{
					let selectQuery = uni.createSelectorQuery().in(this);
					selectQuery.selectAll('.classics-right-item').boundingClientRect(rect=>{
						if(!rect.length){
							setTimeout(()=>{
								this.getItemDistence();
							},10);
							return;
						}
						rect.forEach(it=>{
							this.itemArr.push(it); // 这里获取到的数据是每个item距离页面顶部的数据，以及每个item的自身数据
							resolve();
						})
					}).exec()
				})
			},
		},
		mounted(){
			// 设置一个延时，确保所有dom和样式加载完成，否则拿到的数据可能有误
			setTimeout(()=>{
				this.getItemDistence();
			},500)
			
		},
	}
</script>

<style>
	.classicsBox{
		box-sizing: border-box;
		width: 100%;
		height: 100%;
		display: flex;
		padding-top: 8px;
	}
	.classics-left{
		width: 25%;
		height: 100%;
		box-sizing: border-box;
		padding-right: 6px;
		/* overflow-y: auto; */
	}
	.classics-left-item{
		height: 60px;
		box-sizing: border-box;
		text-align: center;
		line-height: 60px;
		color: black;
		font-weight: 600;
		font-size: 14px;
	}
	.classics-left-item:last-child{
		border: none;
	}
	.classics-right{
		background-color: #fff;
		width: 75%;
		box-sizing: border-box;
		/* overflow-y: auto; */
	}
	.classics-right-item{
		width: 100%;
		box-sizing: border-box;
	}
	.title{
		height: 50px;
		line-height: 50px;
		font-weight: 600;
		font-size: 14px;
		background: url('../../../static/itembackg.png') center center no-repeat ;
		background-size: 100%;
		box-sizing: border-box;
		padding-left: 10px;
		color: #87ff07;
		font-family: 'Courier New', Courier, monospace;
		/* -webkit-text-stroke: 1px #ff55ff; */
	}
	.item-box{
		display: flex;
		width: 100%;
		box-sizing: border-box;
		padding-bottom: 20px;
		padding-left: 10px;
	}
	.item-box-left{
		width: 90px;
		height: 90px;
		background-color: #fafafa;
		border-radius: 8px;
		box-sizing: border-box;
	}
	.item-box-right{
		width: calc(100% - 102px);
		box-sizing: border-box;
		padding-left: 12px;
		position: relative;
		box-sizing: border-box;
		background-color: #fff;
		
	}
	.item-box-right-name,.item-box-right-price{
		color: black;
		font-weight: 600;
		font-size: 14px;
	}
	.item-box-right-describe{
		color: #909090;
		font-size: 12px;
	}
	.item-box-right-buy{
		width: 100%;
		position: absolute;
		bottom: 0;
		display: flex;
		justify-content: space-between;
		box-sizing: border-box;
		padding-right: 12px;
	}
	.item-box-right-pick{
		background: linear-gradient(#ffa7b7,#ffcee4);
		padding: 4px 6px;
		border-radius: 12px;
		color: #ffffff;
		font-size: 12px;
	}
	.checkedStyle{
		background-color: #ffffff;
		border-left: 5px solid #ffb3c8;
		box-sizing: border-box;
		color: #ff797b;
		border-radius: 0 20px 20px 0;
	}
	
</style>