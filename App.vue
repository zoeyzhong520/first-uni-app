<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/* uni.css - 通用组件、模板样式库，可以当作一套ui库应用 */
	@import './common/uni.css';
	@import './common/first-uni-app';
	
	/*每个页面公共css */
	.root_page {
		width: 100%;
		height: 100%;
		background-color: rgb(239,239,239);
		position: absolute;
	}
</style>
