<template>
	<view class="content">
		<view class="leaveItem" v-for="item in leaveList" :key="item.id" @click="toLeaveItem">
			<image class="Pic" :src="item.userPic"></image>
			<view class="center">
				<view class="top">
					<text class="userName">{{item.name}}</text>
					<text class="department">{{item.department}}</text>
				</view>
				<view class="bottom">
					<text class="highlight">{{item.leaveType}} {{item.days}}天 {{item.startTime}}到{{item.endTime}}</text>
					<text class="adopt">{{item.state}}</text>
				</view>
			</view>
			<view class="right">
				<image src="/static/icon/arr.png"></image>
			</view>
		</view>
		<view class="suspension" @click="toIncrease">
			<image src="/static/icon/xinzeng.png"></image>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				leaveList: [
					{
						id: 0,
						userPic: '/static/img/user.jpg',
						name: '周杰伦',
						department: '系部已审核',
						leaveType: '普通事假',
						days: '1',
						startTime: '09-25',
						endTime: '09-25',
						state: '通过'
					},
					{
						id: 1,
						userPic: '/static/img/user.jpg',
						name: '周杰伦',
						department: '班主任通过',
						leaveType: '假期外出',
						days: '1',
						startTime: '09-21',
						endTime: '09-21',
						state: '通过'
					},
					{
						id: 2,
						userPic: '/static/img/user.jpg',
						name: '周杰伦',
						department: '系部已审核',
						leaveType: '普通事假',
						days: '1',
						startTime: '09-18',
						endTime: '09-18',
						state: '通过'
					}
				]
			}
		},
		methods: {
			// 跳转到请假详情	
			toLeaveItem() {
				uni.navigateTo({
					url: '/pages/leaveItem/leaveItem',
					animationType: "slide-in-right",
					animationDuration: 200
				});
			},
			// 跳转到添加请假 
			toIncrease() {
				uni.navigateTo({
					url: '/pages/increase/increase',
					animationType: "slide-in-right",
					animationDuration: 200
				});
			}
		}
	}
</script>

<style>
	.home-nav {
	    background-color: #27ae62;
	    color: #fff;
	    position: fixed;
	    left: 0;
	    right: 0;
	    top: 0;
	    z-index: 9;
	}
	
	.content {
		padding:0 18rpx;
		border-bottom: 6rpx solid #dcdcdc;
	}
	
	.content .leaveItem {
		display: flex;
		padding: 24rpx 0;
		border-top: 3rpx solid #dcdcdc;
	}
	
	.leaveItem .Pic {
		width: 90rpx;
		height: 90rpx;
	}
	
	.leaveItem .center {
		flex: 1;
		display: flex;
		flex-direction: column;
		justify-content: space-around;
		margin: 0 10rpx;
	}
	
	.leaveItem .center .top {
		font-size: 36rpx;
		font-weight: 500;
	}
	
	.center .top text {
		margin-right: 15rpx;
	}
	
	.leaveItem .center .bottom {
		font-size: 24rpx;
		color: #757575;
	}
	
	.center .bottom .highlight {
		color: #fff;
		background-color: #27ae62;
		border-radius: 10rpx;
		padding: 3rpx 8rpx;
		margin-right: 20rpx;
		letter-spacing: 1rpx;
	}
	
	.leaveItem .right {
		margin: auto;
	}
	
	.leaveItem .right image {
		width: 36rpx;
		height: 36rpx;
	}
	
	.suspension {
		position: fixed;
		right: 30rpx;
		bottom: 150rpx;
	}
	
	.suspension image {
		width: 80rpx;
		height: 80rpx;
	}
</style>
