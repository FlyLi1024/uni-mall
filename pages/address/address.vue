<template>
	<view class="address">
		<view class="header">
			<view class="back">
				<text class="iconfont">&#xe660;</text>
				<text>返回</text>
			</view>
			<view class="title">收货地址管理</view>
		</view>
		<view class="address-content">
			<view class="address-item" v-for="(item,index) in 5" :key="index">
				<view class="info">
					<view class="user">
						<text>王小二</text>
						<text>13693343287</text>
					</view>
					<view class="detail">
						<text class="iconfont">&#xe8ae;</text>
						<text>北京市昌平区沙河镇沙阳路20号北京市昌平区沙河镇沙阳路20号</text>
					</view>
				</view>
				<view class="option">
					<view class="default" :class="{' is-default':index===0}">
						<text class="iconfont" v-if="index===0">&#xe6d4;</text>
						<text class="iconfont" v-else>&#xe8c7;</text>
						<text>{{index===0?'默认地址':'设为默认'}}</text>
					</view>
					<view class="edde">
						<view class="edit"><text class="iconfont">&#xe8ac;</text><text>编辑</text></view>
						<view class="delete"><text class="iconfont">&#xe8b7;</text><text>删除</text></view>
					</view>
			
				</view>
			</view>
		</view>
		<view class="add" @click="toEditAddress">添加收货地址</view>
	</view>
</template>

<script>
	export default{
		methods:{
			toEditAddress() {
				uni.navigateTo({
					url: '/pages/address/address-edit/address-edit'
				})
			},
		}
	}
</script>

<style lang="scss" scoped>
	@import '../../style/mixin.scss';
	@import 'address.scss';
</style>
