<template>
	<view class="page-home">
		<view class="status_bar"></view>
		<view class="header">
			<view class="search" @click="onSearch">
				<view class="search-wrap"><text class="iconfont">&#xe651;</text>搜索热门商品</view>
				<view class="iconfont icon-message news"></view>
			</view>
			<view class="hotkey">
				<view class="content">
					<scroll-view scroll-x="true">
						<view class="item actv"><text>推荐</text></view>
						<view class="item"><text>家电</text></view>
						<view class="item"><text>手机</text></view>
						<view class="item"><text>男装</text></view>
						<view class="item"><text>女装</text></view>
						<view class="item"><text>超市</text></view>
						<view class="item"><text>家具</text></view>
						<view class="item"><text>生鲜</text></view>
						<view class="item"><text>水果</text></view>
					</scroll-view>
				</view>
				<view class="more"><text class="iconfont icon-down"></text></view>
			</view>
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
			<view class="nav-item" v-for="(item,index) in 10" :key="index">
				<image :src="`../../static/nav/nav_ico${index+1}.png`" mode="widthFix"></image>
				<text class="text">清场甩货</text>
			</view>
		</view>
		<!-- 公告 -->
		<view class="notice">
			<view class="notice-content">
				<view class="iconfont icon-news"></view>
				<view class="content">
					<swiper class="swiper" :circular="true" :vertical="true" :indicator-dots="false" :autoplay="true" :interval="4000" :duration="1000">
					<swiper-item v-for="(item,index) in 5" :key="index">
						<view class="swiper-item">
							<text class="item">何*** 理刚刚通过推广赚了￥25.00元商品男装休闲装购买</text>
						</view>
					</swiper-item>
					</swiper>
				</view>
				<view class="more">详情</view>
			</view>
		</view>
		<view class="seckill">
			seckill
		</view>
		<view class="recommend">
			<view class="recommend-title">
				
			</view>
			<view class="recommend-content">
				recommend
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

<style lang="scss" scoped>
	@import '../../style/mixin.scss';
	@import './index.scss';
</style>
