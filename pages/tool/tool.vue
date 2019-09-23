<template>
	<view class="root_page">
		<view class="uni-list">
			<!--单独添加一个空cell-->
			<view class="default-empty-cell"></view>
			<view class="uni-list-cell" hover-class="uni-list-cell-hover" 
			v-for="(item,index) in list" :key="index">
					<image class="default-cell-image" src="../../static/icon_frame.png"></image>
					<text class="default-cell-title">{{ item.title }}</text>
			</view>
		</view>
	</view>
</template>

<script>
	/*准备数据*/
	export default {
		data() {
			return {
				list: [
					{
						title: '车架号（VIN）查询车型',
						img: '../../static/icon_frame.png'
					},
					{
						title: '违章查询',
						img: '../../static/icon_illegal.png'
					},
					{
						title: '车辆评估',
						img: '../../static/icon_assessment.png'
					}
				]
			}
		}
	}
</script>

<style>
	
	
	
</style>
