<template>
	<view class="address-edit">
		<view class="header">
			<view class="back">
				<text class="iconfont">&#xe660;</text>
				<text>返回</text>
			</view>
			<view class="title">新增收货地址</view>
			<view class="confirm">完成</view>
		</view>
		<view class="content">
			<view class="location">
				<text class="iconfont">&#xe68c;</text>
				<text>定位到当前位置</text>
			</view>
			<view class="form">
				<view class="item username">
					<text class="text">收货人</text>
					<input type="text" placeholder="请填写姓名" placeholder-class="placeholder"/>
				</view>
				<view class="item phone">
					<text class="text">联系电话</text>
					<input type="number" placeholder="请填写联系电话" placeholder-class="placeholder"/>
				</view>
				<view class="item address">
					<text class="text">配送地址</text>
					<view class="address-select">请选择省、市、区 <text class="iconfont">&#xe65f;</text></view>
				</view>
				<view class="item address-detail">
					<textarea placeholder="请填写详细地址(街道、楼牌号等)" placeholder-class="placeholder"/>
				</view>
			</view>
			<view class="is-default">
				<text>设为默认地址</text>
				<switch checked="true" color="#fe0036"/>
			</view>
		</view>
	</view>
</template>

<script>
</script>

<style lang="scss" scoped>
	@import '../../../style/mixin.scss';
	@import 'address-edit.scss';
</style>
