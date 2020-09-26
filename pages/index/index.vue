<template>
	<view class="content">
		<view class="menu animated fadeIn faster" style="width: 100%;height:170rpx;position: fixed;top: 0;left: 0;z-index: 9999;">
			<view class="topMenu d-flex a-center j-center">
				<view class="text-center">
					<!-- <view class="font-md text-white pt-4">欢迎你 !</view> -->
					<view class="font-lg text-white pr-1 pt-4">鸿云智维</view>
				</view>
			</view>
		</view>
		<!-- 全局分割线 -->
		<!-- <divider></divider> -->
		<view class="" style="background-color: white;height: 20rpx;"></view>
			
		<!-- 列表 -->
		<view class="list mx-1 px-3 pt-1" style="margin-top:150rpx;">
			<view class="listTitle d-flex a-center j-start mb-1">
				<image src="../../static/images/wdxm.png" class="mr-2" style="width: 45rpx;height: 45rpx;" mode=""></image>
				<view class="font-35 mb-1">我的项目</view>
			</view>
			<view class="xiangmu d-flex j-sb px-2">
				<view class="lsitItme d-flex flex-column a-center j-center active" hover-class="main-bg-hover-color">
					<view class="leftImage mb-1"><image src="../../static/images/jd2.jpg" mode=""></image></view>
					<view class="rightName"><text class="font-30">立腾致远科技</text></view>
				</view>
				<view class="lsitItme d-flex flex-column a-center j-center">
					<view class="leftImage mb-1"><image src="../../static/images/jd2.jpg" mode=""></image></view>
					<view class="rightName"><text class="font-30 text-muted">绿化科技</text></view>
				</view>
			</view>
			
		</view>
		<!-- 全局分割线 -->
		<divider></divider>
		<view class="order mx-2 px-2 py-1 pt-2">
			<view class="orderTop d-flex a-center j-sb mb-1">
				<view class="orderTopLeft d-flex a-center j-center">
					<image class="mr-1" src="../../static/images/gongdanguanli.png" style="width:55rpx;height:55rpx;" mode=""></image>
					<view class="font-35 ">工单管理</view>
				</view>
				<view class="orderTopRight d-flex  a-center j-center animated " hover-class="jello" @click="jumpToOrderList">
					<text>全部单据</text>
					<image src="../../static/images/youjt.png" style="width: 40rpx;height: 40rpx;" mode=""></image>
				</view>
			</view>
			
			<view class="orderList d-flex a-center mb-2 border-bottom pb-1">
				<view class="orderLeft" style="padding: 0 260rpx 0 35rpx;">
					<view class="">工单号:12142142</view>
					<view class="">任务名称:检修电镀线</view>
					<view class="">状态:待完成</view>
					<view class="">负责人:钱大剩</view>
				</view>
				<view class="orderRight text-white animated" hover-class="jello" @click="jpOrder">操作</view>
			</view>
			<view class="orderList d-flex a-center">
				<view class="orderLeft" style="padding: 0 260rpx 0 35rpx;">
					<view class="">工单号:12142142</view>
					<view class="">任务名称:检修电镀线</view>
					<view class="">状态:待完成</view>
					<view class="">负责人:钱大剩</view>
				</view>
				<view class="orderRight text-white animated" hover-class="jello">操作</view>
			</view>
		</view>
		<!-- 全局分割线 -->
		<divider></divider>
		<view class="inspection mx-2 px-2 py-1 pt-2">
			<view class="inspectionTop d-flex a-center j-sb mb-1">
				<view class="inspectionTopLeft d-flex a-center j-center">
					<image class="mr-1" src="../../static/images/shebeixunjian5.png" style="width:55rpx;height:55rpx;" mode=""></image>
					<view class="font-35 ">设备巡检</view>
				</view>
				<view class="inspectionTopRight d-flex  a-center j-center animated" hover-class="jello" @click="jumpToinspectionList">
					<text>全部单据</text>
					<image src="../../static/images/youjt.png" style="width: 40rpx;height: 40rpx;" mode=""></image>
				</view>
			</view>
			<view class="inspectionList d-flex a-center mb-2 border-bottom pb-1">
				<view class="inspectionLeft" style="padding: 0 260rpx 0 35rpx;">
					<view class="">任务名称:检修电镀线</view>
					<view class="">负责人:钱大剩</view>
					<view class="">时间:待完成</view>
				</view>
				<view class="inspectionRight text-white animated" hover-class="jello" @click="jpInspection">操作</view>
			</view>
			<view class="inspectionList d-flex a-center">
				<view class="inspectionLeft" style="padding: 0 260rpx 0 35rpx;">
					<view class="">任务名称:检修电镀线</view>
					<view class="">负责人:钱大剩</view>
					<view class="">时间:待完成</view>
				</view>
				<view class="inspectionRight text-white animated" hover-class="jello">操作</view>
			</view>
		</view>
		<!-- 全局分割线 -->
		<divider></divider>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	onLoad() {},
	methods: {
		// 全部工单
		jumpToOrderList(){
			uni.navigateTo({
				url:'../orderList/orderList'
			})
		},
		// 工单详情
		jpOrder() {
			uni.navigateTo({
				url: '../task/task'
			});
		},
		// 全部巡检
		jumpToinspectionList(){
			uni.navigateTo({
				url:'../inspectionList/inspectionList'
			})
		},
		// 巡检
		jpInspection() {
			uni.navigateTo({
				url: '../inspection/inspection'
			});
		}
	}
};
</script>

<style scoped>
	.content {
		width: 100%;
		height: 100%;
		background-color: #f5f5f5;
	}
.topMenu {
	width: 100%;
	height: 170rpx;
	background-color: #344d86;
	background: -webkit-linear-gradient(top, #4f77aa, #344d86);
	/* background: url(../../static/images/1.jpg) no-repeat center center; */
	/* background-size: cover; */
}

.list {
	padding-bottom: 25rpx;
	background-color: #ffffff;
	border-radius: 2rpx;
}

.lsitItme {
	height: 140rpx;
	/* border: 1rpx solid #f1f1f1; */
	border-radius: 2rpx;
	background-color: white;
	padding: 7rpx 10rpx 0 10rpx;
}
.active{
	/* background-color: #344d86;
	color: #FFFFFF;
	border-radius: 5rpx;
	opacity: .8; */
	color: #334d86;
	font-weight: bold;
}
.leftImage {
	width:100rpx;
	height:100rpx;
	border-radius:3rpx;
}

.leftImage image {
	width: 100%;
	height: 100%;
	border-radius:50%;
}


.order {
	padding-bottom: 20rpx;
	background-color: #ffffff;
	border-radius: 20rpx;
	line-height: 1.4;
}
.inspection {
	padding-bottom: 20rpx;
	background-color: #ffffff;
	border-radius: 20rpx;
	line-height: 1.4;
}
.orderRight {
	width: 100rpx;
	height: 60rpx;
	background-color: #344d86;
	border-radius: 5rpx;
	text-align: center;
	line-height: 60rpx;
}
.inspectionRight {
	width: 100rpx;
	height: 60rpx;
	background-color: #344d86;
	border-radius: 5rpx;
	text-align: center;
	line-height: 60rpx;
}
</style>
