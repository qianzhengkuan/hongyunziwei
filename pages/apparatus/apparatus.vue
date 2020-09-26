<template>
	<view class="apparatus py-3 px-5">
		<view class="apLeft d-flex  a-center">
			<text style="width:33.33%;" class="font-35">名称</text><text style="width:33.33%;padding-left:24rpx;" class="font-35">标准值</text><text class="font-35" style="padding-left:54rpx;">实际值</text>
		</view>
		<view class="apcontent text-muted">
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电压</text><text  style="width:33.33%;">10~20v</text><input type="text" placeholder="请填写" value="" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电压发发发刚</text><text  style="width:33.33%;">10~20v</text><input type="text" placeholder="请填写" value="" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电流</text><text  style="width:33.33%;">10~20fafadfafav</text><input type="text" placeholder="请填写"  value="" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电压</text><text  style="width:33.33%;">10~20v</text><input type="text" placeholder="请填写" value="" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电压发发发刚</text><text  style="width:33.33%;">10~20v</text><input type="text" placeholder="请填写" value="" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电流</text><text  style="width:33.33%;">10~20fafadfafav</text><input type="text" placeholder="请填写" value="" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电压</text><text  style="width:33.33%;">10~20v</text><input type="text" value="" placeholder="请填写" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电压发发发刚</text><text  style="width:33.33%;">10~20v</text><input type="text" placeholder="请填写" value="" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
			<view class="apMain d-flex a-center j-sb my-4">
				<text style="width:33.33%;">电流</text><text  style="width:33.33%;">10~20fafadfafav</text><input type="text" placeholder="请填写" value="" class="font-md text-center border-bottom" style="width: 180rpx;"/>
			</view>
		</view>
		
		<view class="confirm d-flex a-center j-sa">
			<view @click="toBack" style="width: 240rpx;" class="d-flex a-center j-center main-bg-color text-white rounded font-lg mb-4 mt-10 animated" hover-class="jello">确认</view>
			<view @click="jumpFq" style="width: 240rpx;" class="d-flex a-center j-center main-bg-color text-white rounded font-lg mb-4 mt-10 animated" hover-class="jello">故障申请</view>
		</view>
		
	</view>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			// 确认后返回巡检详情
			toBack(){
				uni.navigateBack({
					delta:1
				})
			},
			
			// 去故障申请
			jumpFq(){
				uni.navigateTo({
					url:'../Faultrequest/Faultrequest'
				})
			}
		}
	}
</script>

<style>
</style>
