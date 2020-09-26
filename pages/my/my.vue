<template>
	<view class="page">
		<!-- 头部 -->
		<view class="position-relative d-flex a-center animated fadeIn faster" style="height:420rpx;">
			<image src="../../static/images/1.jpg" style="height:420rpx;width: 100%;"></image>
			<view class="d-flex a-center position-absolute left-0 right-0" style="bottom: 50rpx;">
				<image src="../../static/images/zu-copy-copy.png" style="height: 145rpx;width: 145rpx;border: 5rpx solid;" class="rounded-circle border-light ml-4"></image>
				<view class="ml-2 text-white font-md d-flex flex-column"><text class="font-lg">钱大剩</text></view>
			</view>
		</view>

		<!-- 中间 -->
		<view class="main m-2 p-2 rounded-20 mb-5" style="background-color: white;">
			<view class="mainLlist d-flex a-center j-sb border-bottom mb-2 pb-2" @click="myNews">
				<view class="listLeft d-flex a-center j-center">
					<image src="../../static/images/xx.png" style="width: 60rpx;height: 60rpx;" mode=""></image>
					<text class="ml-2 font-35">消息</text>
				</view>
				<view class="listRight"><image src="../../static/images/youjt.png" style="width:45rpx;height:45rpx;" mode=""></image></view>
			</view>
			<view class="mainLlist d-flex a-center j-sb pb-1">
				<view class="listLeft d-flex a-center j-center">
					<image src="../../static/images/sqd.png" style="width: 60rpx;height: 60rpx;" mode=""></image>
					<text class="ml-2 font-35">申请单</text>
				</view>
				<view class="listRight"><image src="../../static/images/youjt.png" style="width:45rpx;height: 45rpx;" mode=""></image></view>
			</view>
		</view>

		<!-- 退出登录 -->
		<view @click="loginOut" style="background-color: white;" class="d-flex a-center j-center py-1 rounded-40 font-35 mb-4 animated m-2 main-text-color" hover-class="fadeIn">
			退出登录
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	methods: {
		myNews() {
			uni.navigateTo({
				url: '../myNews/myNews'
			});
		},
		// 退出登录
		loginOut() {
			uni.showModal({
				title: '是否确认退出登录?',
				// content: '是否确认退出登录?',
				success: function(res) {
					if (res.confirm) {
						console.log('用户点击确定');
					} else if (res.cancel) {
						console.log('用户点击取消');
					}
				}
			});
		}
	}
};
</script>

<style scoped>
.page {
	width: 100%;
	height: 100%;
	background-color: #f5f5f5;
}
</style>
