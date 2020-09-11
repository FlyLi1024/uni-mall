<template>
	<view class="cart" :class="{'not':count <=0}">
		<view class="header"  v-if="count != 0">
			<text>购物车{{count}}</text>
			<view class="edit">管理</view>
		</view>
		<view class="no-cart" :class="{'not':count ===0}" v-if="count === 0">
			<view class="icon"></view>
			<text class="tips">购物车竟然是空的</text>
			<view class="btn">去首页逛逛</view>
		</view>
		
		<view class="has-cart" v-if="count > 0">
			<view class="" v-for="(item,index) in 5" :key="index">
				aaa-{{index}}
			</view>
		</view>
		<view class="count" v-if="count>0">
			<view class="check-total">
				<text class="iconfont">&#xe8df;</text>
				<text>全选</text>
			</view>
			<view class="settlement">
				<view>
					合计<text class="sum">：&yen;50000</text>
				</view>
				<view class="close-account">
					结算（{{count}}）
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			count:0
		};
	},
	onLoad() {
		console.log("cart");
	}
};
</script>

<style lang="scss" scoped>
	@import '../../style/mixin.scss';
	@import './cart.scss';
</style>
