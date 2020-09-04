<template>
	<view>
		<view class="user-header">
			<view class="header-tips">登录一下，与时尚零距离接触！</view>
			<button class="header-login">去登录</button>
		</view>
		<!-- <view class="user-header haslogin">
			<view class="info">
				<view class="pic">
					<image src="../../static/nav/nav1.png"></image>
				</view>
				<text class="userneame">欢迎您：FlyLi</text>
			</view>
			<text class="iconfont">&#xe65f;</text>
		</view> -->
		<view class="my-order">
			<view class="text">
				<!-- <text class="iconfont">&#xe600;</text> -->
				我的订单
			</view>
			<view class="more">
				全部订单
				<text class="iconfont">&#xe65f;</text>
			</view>
		</view>
		<view class="order-status">
			<view class="item">
				<text class="iconfont">&#xe603;</text>
				<text>待付款</text>
			</view>
			<view class="item">
				<text class="iconfont">&#xe602;</text>
				<text>待发货</text>
			</view>
			<view class="item">
				<text class="iconfont">&#xe604;</text>
				<text>待收货</text>
			</view>
			<view class="item">
				<text class="iconfont">&#xe606;</text>
				<text>退款/退货</text>
			</view>
		</view>
		<view class="h20"></view>
		<view class="user-item">
			<view class="text">
				<text class="iconfont">&#xe65a;</text>
				我的优惠券
			</view>
			<view class="more"><text class="iconfont">&#xe65f;</text></view>
		</view>
		<view class="user-item">
			<view class="text">
				<text class="iconfont">&#xe607;</text>
				我的足迹
			</view>
			<view class="more"><text class="iconfont">&#xe65f;</text></view>
		</view>
		<view class="user-item">
			<view class="text">
				<text class="iconfont">&#xe643;</text>
				我的收藏
			</view>
			<view class="more"><text class="iconfont">&#xe65f;</text></view>
		</view>
		<view class="user-item" @click="toSettingPage">
			<view class="text">
				<text class="iconfont">&#xe64b;</text>
				设置中心
			</view>
			<view class="more"><text class="iconfont">&#xe65f;</text></view>
		</view>
		<view class="user-item">
			<view class="text">
				<text class="iconfont">&#xe60c;</text>
				退出登录
			</view>
		</view>
	</view>
</template>
success

<script>
export default{
		methods:{
			toSettingPage() {
				uni.navigateTo({
					url: '/pages/setting/setting'
				})
			},
		}
	}
</script>

<style lang="scss" scoped>
	@import './my.scss';
</style>
