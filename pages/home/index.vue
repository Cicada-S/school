<template>
	<view class="content" @click="toLeaveList">
		<image src="../../static/img/home.jpg" mode="widthFix" class="image" ></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello uniapp'
			}
		},
		onLoad() {

		},
		methods: {
			// 点击跳转到请假列表
			toLeaveList(){
				uni.navigateTo({
					url: '/pages/leaveList/leaveList',
					animationType: "slide-in-right",
					animationDuration: 200
				});
			}
		}
	}
</script>

<style>
	.content image {
		width: 100%;
	}
</style>
