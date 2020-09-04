<template>
	<view class="setting">
		<view class="header">
			<view class="back">
				<text class="iconfont">&#xe660;</text>
				<text>返回</text>
			</view>
			<view class="title">设置</view>
		</view>
		<view class="setting-item" @click="toAddress">
			<text>收货地址管理</text>
			<text class="iconfont">&#xe65f;</text>
		</view>
		<view class="setting-item">
			<text>设置支付密码</text>
			<text class="iconfont">&#xe65f;</text>
		</view>
		<view class="setting-item">
			<text>修改登录密码</text>
			<text class="iconfont">&#xe65f;</text>
		</view>
		<view class="setting-item">
			<text>关于我们</text>
			<text class="iconfont">&#xe65f;</text>
		</view>
	</view>
</template>

<script>
	export default{
		methods:{
			toAddress() {
				uni.navigateTo({
					url: '/pages/address/address'
				})
			},
		}
	}
</script>

<style lang="scss" scoped>
	@import '../../style/mixin.scss';
	@import './setting.scss';
</style>
