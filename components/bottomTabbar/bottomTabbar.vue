<template>
	<u-tabbar v-model="current" :list="list" icon-size="30rpx" height="90rpx" :mid-button="true" inactive-color="#7A7E82" active-color="#FFB51A"></u-tabbar>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
						pagePath: "/pages/home/index",
						iconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/pXnv2MUonVeBfa86b5cd5482fd871615f858f3077322_1647845455959.png",
						selectedIconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/wUIA1GKVyyHG43c16f23db11052aac4e6874bf8c8b44_1647845529867.png",
						text: '首页',
						customIcon: false,
					},
					{
						pagePath: "/pages/wash/index",
						iconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/IPg7gaESXY8wc084defda45c08262dddc30b6d6118f2_1647845614783.png",
						selectedIconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/NUDKoNRKvT89956f0549e83de57b0d7abd8764c25f63_1647845676872.png",
						text: '洗护',
						customIcon: false,
					},
					{
						pagePath: "/pages/release/index",
						iconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/SRgPLXbR5UdLd2a4d8e2ab21e0cd57fca89779ec2b3c_1647845751924.png",
						selectedIconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/SRgPLXbR5UdLd2a4d8e2ab21e0cd57fca89779ec2b3c_1647845751924.png",
						text: '发布',
						midButton: true,
						customIcon: false,
					},
					{
						pagePath: "/pages/planet/index",
						iconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/oEJRi0aS7RH36a8a2519b9c228dadd477f4a67447b6e_1647845777242.png",
						selectedIconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/A0lh3ZsBAjum5671ebfaf8a231eb4f30f76a33696966_1647845804125.png",
						text: '论坛',
						customIcon: false,
					},
					{
						pagePath: "/pages/user/index",
						iconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/Ja3KO3NQxFwP386f0d5f259ed45e4b09d085946e1f9a_1647845829065.png",
						selectedIconPath: "http://kuqichong.oss-cn-beijing.aliyuncs.com/S6IVeoB3mKvS81766e3c3b27da051295a1a779ef0ba8_1647845847526.png",
						text: '我的',
						customIcon: false,
					},
				],
				current: 0
			}
		}
	}
</script>
