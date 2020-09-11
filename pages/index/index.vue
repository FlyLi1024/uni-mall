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
		<view class="carousel">
			<swiper class="carousel-wrap" indicator-dots="true" circular="true" autoplay="true" interval="4000" duration="500">
				<swiper-item v-for="(item,index) in 5" :key="index">
					<image class="carousel-item" src="../../static/banner/banner1.jpg" mode="widthFix"></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="nav">
			<view class="nav-item" v-for="(item,index) in 5" :key="index">
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
		<view class="activity">
			<view class="seckill">
				<view class="row">
					<text class="title">限时抢购</text>
					<view class="time-wrap">
						<text class="time">18</text>
						<text class="sp">:</text>
						<text class="time">50</text>
						<text class="sp">:</text>
						<text class="time">36</text>
					</view>
				</view>
				<view class="desc">限时限量抢半价</view>
				<view class="goods">
					<view class="goods-item">
						<image src="https://image.360kad.com/group2/M00/F5/39/CgAgFF6FyQ-ABcr_AAFgCGfboKk818.jpg_180x180.jpg" mode="widthFix"></image>
					</view>
					<view class="goods-item">
						<image src="https://image.360kad.com/group1/M00/1C/28/CgAgD18aic2AV12xAAJPYg8vvQE684.jpg_180x180.jpg" mode="widthFix"></image>
					</view>
					
				</view>
			</view>
			<view class="new-goods">
				<view class="title">排行榜</view>
				<view class="desc">销量排行推荐</view>
				<image src="https://image.360kad.com/group2/M00/E6/91/CgAgFV4Cv6qAFJNvAAGOwREe1P4233.jpg_180x180.jpg" mode="widthFix"></image>
			</view>
		</view>
		<view class="activity last">
			<view class="new-goods">
				<view class="title">吃货必备</view>
				<view class="desc">缤纷水果趴</view>
				<image src="https://m.360buyimg.com/babel/s333x333_jfs/t19459/183/2418296304/530149/bda1ae1a/5af44331N331fe1b2.png" mode="widthFix"></image>
			</view>
			<view class="new-goods">
				<view class="title">厨房配件</view>
				<view class="desc">厨房神器</view>
				<image src="https://m.360buyimg.com/babel/s333x333_jfs/t1/106136/14/16321/130906/5e79efb8Ea3f08fe2/7caa59c8f11e2c60.jpg!q70.dpg" mode="widthFix"></image>
			</view>
			<view class="new-goods">
				<view class="title">有好货</view>
				<view class="desc">只给挑剔的你</view>
				<image src="https://m.360buyimg.com/ceco/s210x210_jfs/t1/138953/8/4440/197581/5f28cb1eEc217ff27/9d71e5f7679ba3b1.jpg!q70.dpg.webp" mode="widthFix"></image>
			</view>
		</view>
		<view class="recommend">
			<view class="recommend-title">
				猜你喜欢
			</view>
			<view class="recommend-content">
				<view class="goods-item" v-for="(item,index) in 20" :key="index">
					<view class="pic">
						<image :src="`../../static/img/goods_thumb_${index+1}.png`" mode="heightFix"></image>
					</view>
					<view class="title">
						<text class="label">特价</text>
						BANDALY 2020夏季女装连衣裙韩版大码宽松显瘦套装裙子两件套 JX19301 上豆绿下米白 M 
					</view>
					<view class="price">
						<view class="sprice">
							<text class="rmb">&yen;</text>
							<text>12.6</text>
						</view>
						<view class="addcart iconfont icon-cart"></view>
						<!-- <view class="oprice">
							<text class="rmb">&yen;</text>
							<text>35</text>
						</view> -->
					</view>
				</view>
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
