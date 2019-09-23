<template>
	<view class="root_page">
		<view class="uni-list">
			<view class="default-empty-cell"></view>
			<view class="uni-list-cell">
				<input class="default-cell-input" placeholder="请输入验证码" style="height: 40px;"/>
				<!--获取验证码-->
				<button class="sms-button" type="warn" @click="smsAction()">获取验证码</button>
			</view>
		</view>
		<!--确定按钮-->
		<button class="defult-button" type="warn" @click="confirmForm()">确定</button>
	</view>
</template>

<script>
	
	export default {
		data () {
			return {
				
			}
		},
		methods: {
			smsAction () {
				uni.showModal({
					content: '获取验证码',
					showCancel: false
				});
			},
			confirmForm () {
				uni.showModal({
					content: '点击确定',
					showCancel: false
				});
			}
		}
	}
	
</script>

<style>
</style>
