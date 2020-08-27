<template>
	<view class="cart">
		<view class="no-cart">
			<view class="icon"></view>
			<text class="tips">购物车空空如也~</text>
			<view class="btn">去购物</view>
		</view>
		
		<view class="has-cart">
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	onLoad() {
		console.log('cart');
	}
};
</script>

<style lang="scss" scoped>
	@import './cart.scss';
</style>
