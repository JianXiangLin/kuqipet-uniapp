<template>
	<view class="wrap home">
		<!-- 轮播 -->
		<u-swiper :list="banners" keyName="image" :autoplay="true" circular indicator></u-swiper>
		<!-- 我的宠物 -->
		<view class="pets">
			<swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="true" :interval="3000" :duration="500">
				<swiper-item>
					<view class="swiper-item uni-bg-red">A</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item uni-bg-green">B</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item uni-bg-blue">C</view>
				</swiper-item>
			</swiper>
		</view>
		<bottom-tabbar></bottom-tabbar>
	</view>
</template>

<script>
	import {
		BottomTabbar
	} from "@/components/bottomTabbar/bottomTabbar.vue";
	export default {
		components: {
			BottomTabbar
		},
		data() {
			return {
				banners: [{
					image: 'https://cdn.uviewui.com/uview/swiper/swiper2.png',
					title: '昨夜星辰昨夜风，画楼西畔桂堂东',
				}, {
					image: 'https://cdn.uviewui.com/uview/swiper/swiper1.png',
					title: '身无彩凤双飞翼，心有灵犀一点通'
				}, {
					image: 'https://cdn.uviewui.com/uview/swiper/swiper3.png',
					title: '谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳'
				}],
				pets: [
					{
						image: 'https://cdn.uviewui.com/uview/swiper/swiper2.png',
						title: '昨夜星辰昨夜风，画楼西畔桂堂东',
					}, {
						image: 'https://cdn.uviewui.com/uview/swiper/swiper1.png',
						title: '身无彩凤双飞翼，心有灵犀一点通'
					}, {
						image: 'https://cdn.uviewui.com/uview/swiper/swiper3.png',
						title: '谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳'
					}
				],
				currentNum: 0
			}
		},
		onLoad() {
			console.log(this.$userInfo)
		}
	}
</script>

<style lang="scss" scoped>
	.indicator {
		@include flex(row);
		justify-content: center;

		&__dot {
			height: 6px;
			width: 6px;
			border-radius: 100px;
			background-color: rgba(255, 255, 255, 0.35);
			margin: 0 5px;
			transition: background-color 0.3s;

			&--active {
				background-color: #ffffff;
			}
		}
	}

	.indicator-num {
		padding: 2px 0;
		background-color: rgba(0, 0, 0, 0.35);
		border-radius: 100px;
		width: 35px;
		@include flex;
		justify-content: center;

		&__text {
			color: #FFFFFF;
			font-size: 12px;
		}
	}
	
	.pets {
		margin: 40rpx 0;
	}
	.swiper {
		height: 220rpx;
	}
	.swiper-item {
		display: block;
		height: 220rpx;
		line-height: 220rpx;
		text-align: center;
		border-radius: 8rpx;
	}
	.swiper-list {
		margin-top: 40rpx;
		margin-bottom: 0;
	}
	.uni-common-mt {
		margin-top: 60rpx;
		position: relative;
	}
	.info {
		position: absolute;
		right: 20rpx;
	}
	.uni-padding-wrap {
		width: 550rpx;
		padding: 0 100rpx;
	}
	
	.uni-bg-red {
		background-color: red;
	}
	.uni-bg-green {
		background-color: green;
	}
	.uni-bg-blue {
		background-color: blue;
	}
</style>
