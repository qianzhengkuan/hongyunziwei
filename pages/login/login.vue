<template>
	<view class="content">
		<view class="p-5">
			<view class="font-big text-center text-white" style="padding-top: 200rpx;margin-bottom: 150rpx;">账户登录</view>
			<view class="user d-flex">
				<view class="font-lg text-white mr-4">账户</view>
				<input type="text" class="border mb-5 uni-input px-0 p-1 pl-2 rounded" placeholder="请输入账号" placeholder-class="text-light-muted" />
			</view>
			<view class="psd d-flex mb-5">
				<view class="font-lg text-white  mr-4">密码</view>
				<input type="text" class="border mb-5 uni-input px-0 p-1 pl-2 rounded" placeholder="请输入密码" placeholder-class="text-light-muted" />
			</view>
			
			<view @click="login" style="background-color: white;padding: 5rpx 0;" class="d-flex a-center j-center  main-text-color rounded-40 font-lg mb-4 animated" hover-class="fadeIn main-bg-color">登  录</view>
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
			login(){
				uni.switchTab({
					 url:'../index/index'
				})
			}
		}
	}
</script>

<style scoped>
	.content {
		width: 100%;
		height: 100vh;
		background: url("../../static/images/beijing.jpg") no-repeat;
	}
</style>
