<script>
	export default {
		onLaunch: function() {
			uni.onTabBarMidButtonTap(()=>{
				console.log("点击了")
			})
		},
		onShow: function() {
			
		},
		onHide: function() {
			
		},
		
	}
</script>

<style lang="scss">
	/*每个页面公共css */
	@import "@/uni_modules/uview-ui/index.scss";
	@import "common/demo.scss";
	.wrap {
		display: flex;
		flex: 1;
		flex-direction: column;
		background-color: #fff;
		padding: 24rpx 32rpx;
	}
</style>
