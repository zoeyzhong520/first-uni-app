<template>
	<view class="root_page">
		<view class="header">
			<text class="header-title">您好，欢迎您使用中犇-APP</text>
		</view>
		
		<view class="itemsView">
			<text class="itemsTitle">贷前管理</text>
			
			<view class="itemsDetailView">
				<view class="item">
					<image class="itemImg" src="../../static/icon_carloan.png"></image>
					<text class="itemTitle">提交申请</text>
				</view>
				<view class="item">
					<image class="itemImg" src="../../static/mendiandingjia_03.png"></image>
					<text class="itemTitle">车辆定价</text>
				</view>
				<view class="item">
					<image class="itemImg" src="../../static/shenqingshidi.png"></image>
					<text class="itemTitle">申请实地</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	
</script>

<style>
	
	/*头部标题*/
	.header {
		background-color: rgb(239,239,239);
		height: 30px;
	}
	
	.header-title {
		font-size: 15px;
		color: rgb(120,122,123);
		padding-left: 10px;
		line-height: 30px;
		display: block;
	}
	
	/*菜单View*/
	.itemsView {
		background-color: #FFFFFF;
		height: 160px;
	}
	
	/*菜单标题*/
	.itemsTitle {
		font-size: 15px;
		display: block;
		padding: 10px;//设置内边距
	}
	
	/*菜单详情View*/
	.itemsDetailView {
		display: flex;
		flex-direction: row;
	}
	
	/*子菜单*/
	.item {
		width: 33.3%;
		height: 120px;
		text-align: center;
	}
	
	/*子菜单图片*/
	.itemImg {
		display: block;
		width: 60px;
		height: 60px;
		margin: 10px auto;
	}
	
	/*子菜单标题*/
	.itemTitle {
		display: block;
		font-size: 15px;
		line-height: 16px;
	}
	
</style>
