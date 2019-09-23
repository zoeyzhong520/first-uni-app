<template>
	<view class="root_page">
		<view class="uni-list" v-for="(item,index) in list" :key="index">
			<view class="uni-list-cell">
				<view class="default-cell-title">{{ item.title }}</view>
				<view class="default-cell-title-right" style="color: rgb(126,127,128);">{{ item.note }}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data () {
			return {
				list: [
					{
						title: '工号',
						note: '80000000'
					},
					{
						title: '姓名',
						note: '大锤'
					},
					{
						title: '绑定手机号',
						note: '1777777777'
					}
				]
			}
		}
	}
</script>

<style>
</style>
