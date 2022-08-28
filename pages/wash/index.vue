<template>
	<view class="wrap">
		<u-sticky>
			<u-search v-model="mix" :clearabled="true" @search="onSearch"></u-search>
		</u-sticky>
		<view class="u-flex tag">
			<view class="tag-li" v-for="(item, index) in radios" :key="index">
				<u-tag :text="`选项${index + 1}`" :plain="!item.checked" type="warning" :name="index"
					@click="radioClick">
				</u-tag>
			</view>
		</view>
		<bottom-tabbar></bottom-tabbar>
	</view>
</template>

<script>
	import BottomTabbar from '@/components/bottomTabbar/bottomTabbar.vue'
	export default {
		components: {
			BottomTabbar
		},
		data() {
			return {
				mix: '',
				radios: [{
					checked: true
				}, {
					checked: false
				}, {
					checked: false
				}]
			}
		},
		methods: {
			radioClick(name) {
				this.radios.map((item, index) => {
					item.checked = index === name ? true : false
				})
			},
			onSearch(value) {
				console.log(value)
			}
		}
	}
</script>

<style lang="less" scoped>
	.tag {
		padding: 24rpx 0;
		&-li {
			margin-right: 24rpx;
		}
	}
</style>