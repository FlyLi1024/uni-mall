<template>
	<view class="home">
		<view class="status_bar"></view>
		<view class="search-wrap" @click="onSearch">
			<view class="search-box"><text class="iconfont">&#xe651;</text></view>
			<view class="news iconfont">&#xe656;</view>
		</view>
		<view class="banner">
			<swiper class="swiper" indicator-dots="true" circular="true" autoplay="true" interval="4000" duration="500">
				<swiper-item>
					<image class="swiper-item" src="../../static/banner/banner1.jpg" mode="widthFix"></image>
				</swiper-item>
				<swiper-item>
					<image class="swiper-item" src="../../static/banner/banner2.jpg" mode="widthFix"></image>
				</swiper-item>
				<swiper-item>
					<image class="swiper-item" src="../../static/banner/banner3.jpg" mode="widthFix"></image>
				</swiper-item>
				<swiper-item>
					<image class="swiper-item" src="../../static/banner/banner4.jpg" mode="widthFix"></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="nav">
			<view class="nav-item">
				<image src="../../static/nav1.png" mode="widthFix"></image>
				<text class="text">清场甩货</text>
			</view>
			<view class="nav-item">
				<image src="../../static/nav2.png" mode="widthFix"></image>
				<text class="text">活动版块</text>
			</view>
			<view class="nav-item">
				<image src="../../static/nav3.png" mode="widthFix"></image>
				<text class="text">积分兑换</text>
			</view>
			<view class="nav-item">
				<image src="../../static/nav4.png" mode="widthFix"></image>
				<text class="text">套餐服务</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {};
		},
		onLoad() {
			console.log('index');
		},
		methods: {
			/**
			 * 搜索点击
			 */
			onSearch() {
				console.log(123);
				uni.navigateTo({
					url: '/pages/search/search'
				})
			},
		}
	};
</script>

<style lang="less" scoped>
	@import './index.less';
</style>
