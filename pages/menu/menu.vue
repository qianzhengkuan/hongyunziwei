<template>
	<view class="menu">
		<!-- 自定义搜索 -->
		<view class="px-2" style="height:80rpx;background-color: #344d86;padding-top: 70rpx;">
			<view @click="toFaultList" class="flex-1 bg-light rounded d-flex a-center text-light-muted" style="height:65rpx;background-color: #FFFFFF;border-radius:20rpx;">
				<text class="iconfont icon-sousuo mx-2"></text>
				搜索全部及历史故障...
			</view>
	   </view>
	   <!-- 故障列表 -->
	  <view class="menu m-1 px-2">
	  	<view class="menuTop d-flex a-center j-sb mb-1">
	  		<view class="menuTopLeft d-flex a-center j-center">
	  			<image class="mr-1" src="../../static/images/guzhangliebiao.png" style="width:35rpx;height:35rpx;" mode=""></image>
	  			<view class="font-35 ">故障列表</view>
	  		</view>
	  		<view class="menuTopRight d-flex  a-center j-center animated " hover-class="jello" @click="toFaultList">
	  			<text>全部单据</text>
	  			<image src="../../static/images/youjt.png" style="width: 40rpx;height: 40rpx;" mode=""></image>
	  		</view>
	  	</view>
	  	
	  	<view class="menuList d-flex a-center mb-2 border-bottom pb-1">
	  		<view class="menuLeft" style="padding: 0 280rpx 0 35rpx;">
	  			<view class="">设备名称:12142142</view>
	  			<view class="">设备编号:检修电镀线</view>
	  			<view class="">故障描述</view>
	  			<view class="">负责人:钱大剩</view>
	  		</view>
	  		<view class="menuRight text-white animated" hover-class="jello">维修中</view>
	  	</view>
	  	<view class="menuList d-flex a-center">
	  		<view class="menuLeft" style="padding: 0 280rpx 0 35rpx;">
	  			<view class="">设备名称:检修电镀线</view>
	  			<view class="">设备编号:fafadfafag</view>
	  			<view class="">故障描述</view>
	  			<view class="">负责人:钱大剩</view>
	  		</view>
	  		<view class="menuRight text-white animated" hover-class="jello">维修中</view>
	  	</view>
	  </view>
	
	  <!-- 新增故障 -->
	  <view class="newsGz d-flex a-center j-center my-2">
	  	 <view @click="toFaultrequest" class="d-flex flex-column a-center j-center text-white" style="width: 120rpx;height:120rpx;background-color:#344d86;border-radius: 50%;">
	  	 	 <image src="../../static/images/hao.png" style="width:40rpx;height:40rpx;" mode=""></image>
			 <text class="line-h-sm font-sm">故 障</text>
			 <text class="line-h-sm font-sm">申 请</text>
	  	 </view>
	  </view>
	  <!-- 全局分割线 -->
	  <divider></divider>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		},
		mounted() {
			
		},
		methods:{
			//新增故障
			toFaultrequest(){
				uni.navigateTo({
					url:'../Faultrequest/Faultrequest'
				})
			},
			//故障列表
			toFaultList(){
				uni.navigateTo({
					url:'../faultList/faultList'
				})
			},
		}
	}
</script>

<style scoped>
	.menuRight {
		width: 120rpx;
		height: 60rpx;
		background-color:#41a863;
		border-radius:40rpx;
		text-align: center;
		line-height: 60rpx;
	}
</style>
