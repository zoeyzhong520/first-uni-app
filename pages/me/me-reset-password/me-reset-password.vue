<template>
	<view class="root_page">
		<view class="default-empty-cell"></view>
		<view class="uni-list">
			<view class="uni-list-cell">
				<view class="default-cell-title" style="width: 25%;">新密码</view>
				<input class="default-cell-input" placeholder="请输入您的新密码" />
			</view>
			<view class="uni-list-cell">
				<view class="default-cell-title" style="width: 25%;">确认新密码</view>
				<input class="default-cell-input" placeholder="再次输入您的密码" />
			</view>
			<view class="uni-list-cell">
				<view class="default-cell-title" style="width: 25%;">验证码</view>
				<input class="default-cell-input" placeholder="请输入验证码" style="width: 40%;" />
				<!--获取验证码按钮-->
				<button class="sms-button" type="warn" v-on:click="smsAction()">获取验证码</button>
			</view>
		</view>
		
		<!--确定按钮-->
		<button class="defult-button" type="warn"  v-on:click="confirmForm()">确定</button>
		
		<!--用户须知-->
		<text  class="rule-text">{{ rule }}</text>
	</view>
</template>

<script>
	export default {
		data () {
			return {
				rule: '根据相关监管规定，用户需设置并妥善保管账户密码，并定期更换，以确认账户资金安全。\n\n密码设置规则：\n\n1.密码必须包含2种字符组合且长度在8位以上\n2.不得使用曾经设置过的密码\n3.密码有效期为180天，超时后需更换'
			}
		},
		methods: {
			confirmForm () {
				uni.showModal({
					content: '点击确定',
					showCancel: false
				});
			},
			smsAction () {
				uni.showModal({
					content: '获取验证码',
					showCancel: false
				});
			}
		}
	}
</script>
	
<style>
	
	.rule-text {
		margin-left: 10px;
		margin-right: 10px;
		margin-top: 60px;
		display: block;
		color: rgb(173,174,175);
		font-size: 13px;
	}
	
</style>
