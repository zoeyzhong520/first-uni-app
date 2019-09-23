<template>
	<view class="root_page">
		<!--标题-->
		<view class="uni-list-cell">
			<text style="font-size: 13px;margin-left: 10px;margin-right: 10px;">{{ title }}</text>
		</view>
		
		<!--列表-->
		<view class="uni-list">
			<view class="uni-list-cell" hover-class="uni-list-cell-hover" 
			v-for="(item,index) in list" :key="index">
				<view class="uni-title" style="margin-left: 10px;">
					{{ item.title }}
					<text>\n{{ item.subTitle }}</text>
				</view>
				<image class="default-cell-image-right" src="../../../static/myCenter_arrow.png"></image>
			</view>
		</view>
	</view>
</template>

<script>
	
	export default {
		onNavigationBarButtonTap(val) {
			var pages = getCurrentPages();
			var page = pages[pages.length - 1];
			// #ifdef APP-PLUS
			let currentWebview = page.$getAppWebview();
			let titleObject = currentWebview.getStyle().titleNView;
			if (!titleObject.buttons) {
				return
			}
			if (titleObject.buttons[0].text == '编辑') {
				titleObject.buttons[0].text = '完成';
				this.isEdit = true;
			} else {
				titleObject.buttons[0].text = '编辑';
				this.isEdit = false;
			}
			currentWebview.setStyle({
				titleNView: titleObject
			})
			// #endif
		},
		data () {
			return {
				isEdit: false;//是否处于编辑模式
				title: '你可以删除列表中的设备，删除后在该设备登录时需要进行短信验证',
				list: [
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					},
					{
						title: 'MX4',
						subTitle: '2019-09-11 17:37:47'
					}
				]
			}
		}
	}
	
</script>

<style>
	
	.title {
		color: rgb(126,128,129);
		background-color: rgb(239,240,241);
		display: block;
		margin-left: 10px;
		margin-right: 10px;
	}
	
</style>
