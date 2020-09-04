<template>
	<view class="search fadeInTop">
		<view class="search-header">
			<view class="search-wrap fadeInTop">
				<view class="iconfont icon-left"></view>
				<view class="input-box">
					<view class="icon"></view>
					<input type="text" @focus="focus = true" @blur="focus = false" v-model="keyword" placeholder="请输入搜索..." placeholder-style="color:#999" />
					<view class="close" v-if="keyword.length > 0"></view>
				</view>
				<view class="search-btn fadeInTop">搜索</view>
			</view>
		</view> 
		<view class="search-not"></view>
		<view class="search-list" v-show="keyword.length > 0">
			<scroll-view scroll-y style="height: 100vh;" :class="keyword.length > 0 ? 'fadeInTop' : 'fadeOut'">
				<view class="item">暂无相关内容</view>
				<view class="item" v-for="(item,index) in 50" :key="index" @click="handleClick(keyword,index)">搜索结果{{index}}-{{ keyword }}</view>
				<view class="h150"></view>
			</scroll-view>
		</view>
		<view class="search-body">
			<view class="search-recommend fadeInTop" v-if="keyword.length <= 0">
				<view class="title">
					<text>搜索历史</text>
					<text class="clear">清空</text>
				</view>
				<view class="recommend-list history">
					<view class="recommend-item" @click="change">雅漾喷雾<text class="iconfont icon-close"></text></view>
					<view class="recommend-item">理肤泉<text class="iconfont icon-close"></text></view>
					<view class="recommend-item">雅漾<text class="iconfont icon-close"></text></view>
					<view class="recommend-item">喷雾<text class="iconfont icon-close"></text></view>
					<view class="recommend-item">理肤泉喷雾<text class="iconfont icon-close"></text></view>
					<view class="recommend-item">理肤泉B5<text class="iconfont icon-close"></text></view>
					<view class="recommend-item">面膜<text class="iconfont icon-close"></text></view>
					<view class="recommend-item">兰芝<text class="iconfont icon-close"></text></view>
				</view>
			</view>
			<view class="search-recommend fadeInTop" v-if="keyword.length <= 0">
				<view class="title">
					<text>热门搜索</text>
					<text class="clear iconfont icon-refresh"></text>
				</view>
				<view class="recommend-list">
					<text class="recommend-item" @click="change">雅漾喷雾</text>
					<text class="recommend-item">理肤泉</text>
					<text class="recommend-item">雅漾</text>
					<text class="recommend-item">喷雾</text>
					<text class="recommend-item">理肤泉喷雾</text>
					<text class="recommend-item">理肤泉B5</text>
					<text class="recommend-item">面膜</text>
					<text class="recommend-item">兰芝</text>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
export default {
	data() {
		return {
			focus: false,
			keyword: ''
		};
	},
	methods: {
		handleClick(keyword,index){
			uni.showToast({
				title:`你点击了第${index}：${keyword}`,
				mask:true,
				icon:'none'
			})
			this.keyword = '';
		}
	}
};
</script>

<style lang="scss" scoped>
	@import '../../style/mixin.scss';
	@import '../../style/animate.scss';
	@import './search.scss';
</style>
