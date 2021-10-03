<template>
	<view class="content">
		<view class="item" v-for="(item, index) in infoListData" :key="index">
			<view class="left">
				{{index+1}}、{{item.key}}
			</view>
			<view class="right">
				<image v-if="index == 2" :src="item.value" mode=""></image>
				<text v-else>{{item.value}}</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				infoListData: [
					{
						key: '学期',
						value: '2021-2022-第一学期'
					},{
						key: '学生申请状态',
						value: '系部已审核'
					},{
						key: '学生头像',
						value: '/static/img/user.jpg'
					},{
						key: '请假类型',
						value: '普通事假'
					},{
						key: '是否外出',
						value: '是'
					},{
						key: '开始时间',
						value: '2021-09-25'
					},{
						key: '开始节次',
						value: '下午1节 ( 14:40-15:20 )'
					},{
						key: '结束时间',
						value: '2021-09-25'
					},{
						key: '结束节次',
						value: '晚上1节 ( 19:10-19:50 )'
					},{
						key: '请假天数',
						value: 1
					},{
						key: '最终审核状态',
						value: '通过'
					},{
						key: '宿舍楼',
						value: '8栋'
					},{
						key: '床位号',
						value: '5'
					},{
						key: '学生宿舍',
						value: '8-537'
					},{
						key: '原因',
						value: '去打疫苗'
					},{
						key: '附件',
						value: ''
					},{
						key: '班长姓名',
						value: '单向阳'
					},{
						key: '班长学号',
						value: '20181591'
					},{
						key: '请假申请日期',
						value: '2021-09-25 14:40:09'
					},{
						key: '学生申请时间',
						value: '2021-09-25 14:40:09'
					},{
						key: '医务室审核状态',
						value: ''
					},{
						key: '医务室审核时间',
						value: ''
					},{
						key: '医务室审核人',
						value: ''
					},{
						key: '医务室审核意见',
						value: ''
					},{
						key: '班主任审核状态',
						value: '通过'
					},{
						key: '班主任审核时间',
						value: '2021-09-25 14:42:24'
					},{
						key: '班主任审核人',
						value: '方楚华'
					},{
						key: '班主任审核意见',
						value: '同意去狮岭体育馆打疫苗'
					},{
						key: '系部审核状态',
						value: '通过'
					},{
						key: '系部审核时间',
						value: '2021-09-25 15:02:40'
					},{
						key: '系部审核人',
						value: '张震'
					},{
						key: '系部审核意见',
						value: '同意'
					},{
						key: '学工审核状态',
						value: ''
					},{
						key: '学工审核时间',
						value: ''
					},{
						key: '学工审核人',
						value: ''
					},{
						key: '学工审核意见',
						value: ''
					},{
						key: '分管校长审核状态',
						value: ''
					},{
						key: '分管校长审核时间',
						value: ''
					},{
						key: '分管校长审核人',
						value: ''
					},{
						key: '分管校长审核意见',
						value: ''
					},{
						key: '年龄',
						value: '18'
					},{
						key: '学生手机',
						value: '15089557026'
					},{
						key: '家长手机',
						value: '15119639728'
					},{
						key: '外出地点',
						value: '狮岭体育馆'
					},
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	image {
		width: 90rpx;
		height: 90rpx;
	}
	
	.content {
		margin-bottom: 100rpx;
	}
	
	.content .item {
		display: flex;
		font-size: 26rpx;
		padding: 10rpx 0;
		border-bottom: 3rpx solid #dcdcdc;
	}
	
	.content .item:nth-child(3) .right {
		padding: 0 0 0 20rpx;
	}
	
	.item .left {
		flex: 1;
		color: #27ae62;
		padding: 28rpx 0;
		text-align: right;
	}
	
	.item .right {
		flex: 2;
		color: #737373;
		padding: 28rpx 0 28rpx 20rpx;
	}
</style>
