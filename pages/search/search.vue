<template>
	<view class="search fadeInTop">
		<view class="search-header">
			<view class="search-wrap fadeInTop">
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
			<scroll-view scroll-y style="height: 100vh" :class="keyword.length > 0 ? 'fadeInTop' : 'fadeOut'">
				<view class="item">暂无相关内容</view>
				<view class="item" v-for="(item,index) in 10" :key="index" @click="getList(keyword)">搜索结果-{{ keyword }}</view>
				<view class="h128"></view>
			</scroll-view>
		</view>
		<view class="search-recommend fadeInTop" v-if="keyword.length <= 0">
			<view class="title">推荐搜索</view>
			<view class="recommend-list">
				<text class="recommend-item" @click="change">雅漾喷雾</text>
				<text class="recommend-item">理肤泉</text>
				<text class="recommend-item">雅漾</text>
				<text class="recommend-item">喷雾</text>
				<text class="recommend-item">水</text>
				<text class="recommend-item">理肤泉喷雾</text>
				<text class="recommend-item">理肤泉B5</text>
				<text class="recommend-item">面膜</text>
				<text class="recommend-item">兰芝</text>
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
		getList(keyword){
			uni.showToast({
				title:'你点击了：'+keyword,
				mask:true,
				icon:'none'
			})
			this.keyword = '';
		}
	}
};
</script>

<style lang="less" scoped>
	@import '../../style/mixin.less';
	@import '../../style/animate.less';
	@import './search.less';
</style>
