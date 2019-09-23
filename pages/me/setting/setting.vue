<template>
	<view class="root_page">
		<view class="uni-list">
			<view class="uni-list-cell" hover-class="uni-list-cell-hover"
			v-for="(item,index) in list" :key="index" @click="goDetail(index)">
			<text class="default-cell-title">{{ item }}</text>
			<image class="default-cell-image-right" src="../../../static/myCenter_arrow.png"></image>
			</view>
			
			<!--单独处理当前版本行-->
			<view class="uni-list-cell">
				<text class="default-cell-title">当前版本</text>
				<text class="default-cell-title-right">1.0.0</text>
			</view>
		</view>
		
		<button class="defult-button" type="warn" v-on:click="loginOut()">退出登录</button>
	</view>
</template>

<script>
	export default {
		data () {
			return {
				list: ['我的账号','密码修改','修改手势密码','设备管理']
			}
		},
		methods: {
			loginOut () {
				uni.showModal({
					content: '点击退出登录',
					showCancel: false
				});
			},
			goDetail (el) {
				var that = this;
				if (el == 0) {
					//我的账号
					that.showAccount()
				}
				if (el == 1) {
					//密码修改
					that.showResetPassword()
				}
				if (el == 2) {
					//修改手势密码
					that.showResetGesturePassword()
				}
				if (el == 3) {
					//设备管理
					that.showEquipmentManage()
				}
				
			},
			showAccount () {
				uni.navigateTo({
					url: '../me-account/me-account'
				});
			},
			showResetPassword () {
				uni.navigateTo({
					url: '../me-reset-password/me-reset-password'
				})
			},
			showResetGesturePassword () {
				uni.navigateTo({
					url: '../me-reset-gesture-password/me-reset-gesture-password'
				})
			},
			showEquipmentManage() {
				uni.navigateTo({
					url: '../me-equipment-manage/me-equipment-manage'
				})
			}
 		}
	}
</script>

<style>
</style>
