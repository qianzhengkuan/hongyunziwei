<template>
	<view class="Faultrequest p-2">
		<view class="ticket text-center">
			<view class="gzmc d-flex m-1">
				<text class="font-35" style="width:160rpx;">故障名称</text>
				<input v-model="faultName" class="flex-1 border-bottom" type="text" value="" />
			</view>
			<view class="gzmc d-flex m-1">
				<text class="font-35" style="width:160rpx;">设备名称</text>
				<input v-model="deviceName" class="flex-1 border-bottom" type="text" value="" />
			</view>
			<view class="gzmc d-flex m-1" @click="changeMajor" style="position: relative;">
				<text class="font-35" style="width:160rpx;">专业</text>
				<input class="flex-1 border-bottom" type="text" v-model="major" placeholder="请选择" />
				<image src="../../static/images/xxjt.png" style="width: 30rpx;height: 30rpx;position: absolute;top: 0;right:24rpx;" mode=""></image>
			</view>
			<view class="gzmc d-flex m-1" @click="changeFaultLevel" style="position: relative;">
				<text class="font-35" style="width:160rpx;">故障等级</text>
				<input class="flex-1 border-bottom" type="text" v-model="faultLevel" placeholder="请选择" />
				<image src="../../static/images/xxjt.png" style="width: 30rpx;height: 30rpx;position: absolute;right:-20rpx;top: 0;" class="mr-4" mode=""></image>
			</view>
			<view class="gzmc d-flex m-1 " @click="changeFaultSource" style="position: relative;">
				<text class="font-35" style="width:160rpx;">故障来源</text>
				<input class="flex-1 border-bottom" type="text" v-model="faultSource" placeholder="请选择" />
				<image src="../../static/images/xxjt.png" style="width: 30rpx;height: 30rpx;position: absolute;right:-20rpx;top: 0;" class="mr-4" mode=""></image>
			</view>
			<view class="gzmc d-flex m-1">
				<text class="font-35" style="width:160rpx;">发现人</text>
				<input v-model="findMan" class="flex-1 border-bottom" type="text" value="" />
			</view>

			<!-- <picker mode="date" :value="findTime" @change="ChangefindTime">
				<view class="gzmc d-flex m-1" style="position: relative;">
					<text class="font-35" style="width:160rpx;">发现时间</text>
					<input v-model="findTime" class="flex-1 border-bottom" type="text" value="" />
					<image src="../../static/images/xxjt.png" style="width: 30rpx;height: 30rpx;position: absolute;right:-20rpx;top: 0;"
					 class="mr-4" mode=""></image>
				</view>
			</picker> -->
			<view class="gzmc d-flex m-1" style="position: relative;">
				<text class="font-35" style="width:160rpx;">发现时间</text>
				<input v-model="findTime" class="flex-1 border-bottom" type="text" value="" />
			</view>

			<!-- <picker mode="time" :value="handlingTime" @change="ChangehandlingTime">
				<view class="gzmc d-flex m-1" style="position: relative;">
					<text class="font-35" style="width:160rpx;line-height: 32rpx;">要求处理时间</text>
					<input  v-model="handlingTime" class="flex-1 border-bottom" type="text" value="" />
					<image src="../../static/images/xxjt.png" style="width: 30rpx;height: 30rpx;position: absolute;right:-20rpx;top: 0;"
					 class="mr-4" mode=""></image>
				</view>
			</picker> -->
			<view class="gzmc d-flex m-1" style="position: relative;">
				<text class="font-35" style="width:160rpx;line-height: 32rpx;">要求处理时间</text>
				<input v-model="handlingTime" class="flex-1 border-bottom" type="text" value="" />
			</view>
			<!-- 现象描述 -->
			<view class="text-left mb-3 mx-1">
				<text class="font-35 ml-1">现象描述:</text>
				<view class="textbox">
					<textarea
						class="inp_x"
						v-model="describe"
						placeholder-style="font-size:30upx;font-family:PingFang SC;font-weight:500;"
						placeholder="故障现象描述~"
						maxlength="100"
					/>
				</view>
			</view>
			<!-- 上传图片 -->
			<view class="text-left mx-1">
				<text class="font-35 ml-1 mb-2">添加图片</text>
				<view @click="upload" style="width: 180rpx;height: 180rpx;" class="border d-flex a-center j-center ml-1">
					<image src="../../static/images/zengjia01.png" style="width:50rpx;height:50rpx;" mode=""></image>
				</view>
				<view class="touxiangicon"><image class="huiyuan_img" style="width: 180rpx;height: 180rpx;" :src="image" mode=""></image>
				</view>
			</view>
			
			<!-- 提交申请单 -->
			<view @click="login" style="background-color:#344d86;padding: 5rpx 0;position: fixed;bottom:0;left:200rpx;right: 0;width:50%;height: 60rpx;" 
			class="d-flex a-center j-center text-white rounded-40 font-lg mb-4 animated" 
			hover-class="fadeIn main-bg-color">提  交</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			faultName: '', //故障名称
			deviceName: '', //设备名称
			major: '', //专业
			faultLevel: '', //故障等级
			faultSource: '', //故障来源
			findMan: '', //发现人
			findTime: '', //发现时间
			handlingTime: '', //要求处理时间
			describe: '', //现象描述

			image: '',
			showChooseImage: true //是否显示点击上传图片
		};
	},
	methods: {
		// 修改专业
		changeMajor() {
			let MajorArray = ['电气', '暖通', '若电', '其他'];
			uni.showActionSheet({
				itemList: MajorArray,
				success: res => {
					this.major = MajorArray[res.tapIndex];
				}
			});
		},
		// 修改故障等级
		changeFaultLevel() {
			let FaultLevelArray = ['紧急缺陷', '重大缺陷', '一般缺陷', '其他问题'];
			uni.showActionSheet({
				itemList: FaultLevelArray,
				success: res => {
					this.faultLevel = FaultLevelArray[res.tapIndex];
				}
			});
		},
		// 修改故障来源
		changeFaultSource() {
			let FaultSourceArray = ['客户填报', '巡检填报', '其他'];
			uni.showActionSheet({
				itemList: FaultSourceArray,
				success: res => {
					this.faultSource = FaultSourceArray[res.tapIndex];
				}
			});
		},
		// 修改发现时间
		ChangefindTime(e) {
			this.findTime = e.detail.value;
		},
		// 修改要求处理时间
		ChangehandlingTime(e) {
			this.handlingTime = e.detail.value;
		},
		//上传图片
		upload() {
			uni.chooseImage({
				count:9,
				sizeType: ['original', 'compressed'], //可以指定是原图还是压缩图，默认二者都有
				sourceType: ['album','camera'], //从相册选择
				success: function(res) {
					const tempFilePaths = res.tempFilePaths;
					this.image = tempFilePaths[0];
					console.log('tempFilePaths[0]', tempFilePaths[0]); //能够打印出选中的图片
					this.iconcheck = 1; //点击后图片更改状态由0变成1
				},
				error: function(e) {
					console.log(e);
				}
			});
		}
	}
};
</script>

<style scoped>
.textbox {
	margin-top: 10upx;
	padding: 20upx 20upx;
	background-color: #f5f5f5;
	border-radius: 15px;
	height: 190rpx;
}
uni-textarea {
	width: 300px;
	height: 100px;
	display: block;
	position: relative;
	font-size: 16px;
	line-height: normal;
	white-space: pre-wrap;
	word-break: break-all;
}
</style>
