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
		<view class="work_classification">
			<view class="word_block">
				<view class="word_card" @click="goToFoster">
					<image src="https://kuqichong.oss-cn-beijing.aliyuncs.com/bb.png"></image>
					<view>签到福利</view>
				</view>
				<view class="word_card" @click="goToPetShop">
					<image src="https://kuqichong.oss-cn-beijing.aliyuncs.com/bb.png"></image>
					<view>宠物养成</view>
				</view>
				<view class="word_card" @click="goToPetWorld">
					<image src="https://kuqichong.oss-cn-beijing.aliyuncs.com/bb.png"></image>
					<view>吃喝玩乐</view>
				</view>
				<view class="word_card" @click="goToShoppingMall">
					<image src="https://kuqichong.oss-cn-beijing.aliyuncs.com/bb.png"></image>
					<view>萌宠摄影</view>
				</view>
			</view>
		</view>
		<view class="box">
			<view class="box-title">
				<view class="box-title-left">
					附近宠物群聊
				</view>
				<view class="box-title-right">
					<text>进去逛逛</text>
					<u-icon name="arrow-right"></u-icon>
				</view>
			</view>
			<view class="box-ul">
				<view class="box-ul-li">
					<image class="box-ul-li-avatar" src="https://kuqichong.oss-cn-beijing.aliyuncs.com/bb.png" mode="aspectFill"></image>
					<text>群聊名称1</text>
				</view>
				<view class="box-ul-li">
					<image class="box-ul-li-avatar" src="https://kuqichong.oss-cn-beijing.aliyuncs.com/bb.png" mode="aspectFill"></image>
					<text>群聊名称2</text>
				</view>
			</view>
		</view>
		<view class="box">
			<view class="box-title">
				<view class="box-title-left">
					Q&A宠物问答
				</view>
				<view class="box-title-right">
					<text>帮他解答</text>
					<u-icon name="arrow-right"></u-icon>
				</view>
			</view>
			<view class="box-ul">
				<view class="box-ul-li">
					<image class="box-ul-li-avatar" src="https://kuqichong.oss-cn-beijing.aliyuncs.com/bb.png" mode="aspectFill"></image>
					<view class="box-ul-li-info">
						<view>昵称</view>
						<view class="des">签名信息：金毛是我的喜爱</view>
					</view>
				</view>
			</view>
			<view class="box-qs">
				<view class="box-qs-name">
					狗子这样是不是生病了？
				</view>
				<view class="box-qs-des">
					根据张三的研究报告表明，养宠物可以给人带来快乐，养宠物可以给人带来快乐，你同意吗？
				</view>
				<image class="img" src="http://kuqichong.oss-cn-beijing.aliyuncs.com/活动专区_1653489815619.jpg" mode="widthFix"></image>
			</view>
		</view>
		<view class="box">
			<view class="box-title">
				<view class="box-title-left">
					PK 赢奖品
				</view>
				<view class="box-title-right">
					<text>99人已参与</text>
					<u-icon name="arrow-right"></u-icon>
				</view>
			</view>
			<view class="box-qs">
				<view class="box-qs-name">
					养宠物可以带来快乐吗？
				</view>
				<view class="box-qs-des">
					根据张三的研究报告表明，养宠物可以给人带来快乐，养宠物可以给人带来快乐，你同意吗？
				</view>
				<view class="box-qs-btn">
					<view class="box-qs-btn-yes">
						可以
					</view>
					<view class="box-qs-btn-pk">
						PK
					</view>
					<view class="box-qs-btn-no">
						不可以
					</view>
				</view>
			</view>
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
	
	.work_classification {
		.word_block {
			display: flex;
			margin-bottom: 40rpx ;
			.word_card {
				text-align: center;
				font-size: 24rpx;
				width: 25%;
			}
	
			.word_card image {
				height: 90rpx;
				width: 90rpx;
			}
		}
	}
	.box {
		padding: 24rpx;
		box-shadow: $uni-box-shadow-primary;
		border-radius: 8rpx;
		margin-bottom: 40rpx;
		&-title {
			display: flex;
			justify-content: space-between;
			align-items: center;
			&-left {
				border: 2rpx solid #BEC2CB;
				padding: 10rpx 22rpx;
				border-radius: 40rpx;
			}
			&-right {
				font-size: 28rpx;
				font-family: PingFangSC-Regular, PingFang SC;
				font-weight: 400;
				color: #666666;
				line-height: 28rpx;
				display: flex;
				align-items: center;
			}
		}
		&-ul {
			padding-top: 16rpx;
			font-size: 28rpx;
			&-li {
				display: flex;
				align-items: center;
				padding: 12rpx 0;
				&-avatar {
					width: 72rpx;
					height: 72rpx;
					margin-right: 8rpx;
				}
				&-info {
					.des {
						color: #808080;
						font-size: 26rpx;
					}
				}
			}
		}
		&-qs {
			&-name {
				padding: 12rpx 0;
			}
			&-des {
				font-size: 28rpx;
				font-family: PingFangSC-Regular, PingFang SC;
				font-weight: 400;
				color: #333333;
				line-height: 44rpx;
			}
			.img {
				width: 100%;
				margin-top: 12rpx;
			}
			&-btn {
				padding: 20rpx 24rpx 0;
				justify-content: space-between;
				align-items: center;
				display: flex;
				&-yes, &-no {
					width: 168rpx;
					text-align: center;
					border: 2rpx solid #BEC2CB;
					border-radius: 8rpx;
					height: 64rpx;
					line-height: 60rpx;
				}
				&-pk {
					padding: 24rpx;
					border-radius: 50%;
					border: 2rpx solid #BEC2CB;
				}
			}
		}
	}
</style>
