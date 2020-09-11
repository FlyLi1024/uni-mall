<template>
	<view class="category">
		<view class="category-header">
			<!-- <image src="../../static/banner/banner1.jpg" mode="widthFix"></image> -->
		</view>
		<view class="category-content">
			<view class="item">
				<text>热门推荐</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>手机数码</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>电脑办公</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>美妆护肤</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>个护清洁</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>男装</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>男鞋</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>女装</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>女鞋</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>食品生鲜</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>酒水饮料</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>运动户外</text>
				<text class="iconfont icon-right"></text>
			</view>
			<view class="item">
				<text>食品生鲜</text>
				<text class="iconfont icon-right"></text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				aaa: 'asdasd'
			};
		},
		mounted(){
			this.aa();
		},
		methods:{
			aa(){
				var a =1;
				var b=2;
				a==b&&(a=3,b=4)
				console.log(a)
			}
		}
	}
</script>

<style lang="scss" scoped>
	@import '../../style/mixin.scss';
	@import './category.scss';
</style>
