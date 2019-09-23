<template>
	<view class="root_page">
		<view class="uni-list">
			<view class="uni-list-cell" hover-class="uni-list-cell-hover" @click="goDetail()">
				<image class="default-cell-image" src="../../static/icon_setup.png"></image>
				<text class="default-cell-title">{{ item }}</text>
				<image class="default-cell-image-right" src="../../static/myCenter_arrow.png"></image>
			</view>
		</view>
	</view>
</template>

<script>
	
	export default {
		data () {
			return {
				item: '设置'
			}
		},
		onLoad () {
			
		},
		methods: {
			goDetail () {
				uni.navigateTo({
					url: 'setting/setting',
					success: () => {},
					fail: () => {},
					complete: () => {}
				});
			}
		}
	}
	
</script>

<style>
</style>
