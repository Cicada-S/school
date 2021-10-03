<template>
	<view class="content">
		<view class="item" v-for="(item, index) in listData" :key="index">
			<view class="title">
				{{index+1}}、{{item.title}}
			</view>
			<view class="value">
				<input type="text" :placeholder="item.value" />
			</view>
		</view>
		<button type="default" @click="preservation">保存</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				listData: [
					{
						title: '学期',
						value: '2021-2022-第一学期',
					},{
						title: '学生申请状态',
						value: '系部已审核/班主任通过 对应下面请假类型',
					},{
						title: '请假类型',
						value: '普通事假/假期外出',
					},{
						title: '你的姓名',
						value: '周杰伦',
					},{
						title: '开始时间',
						value: '2021-01-01'
					},{
						title: '开始节次',
						value: '请参考正版'
					},{
						title: '结束时间',
						value: '2021-01-01'
					},{
						title: '结束节次',
						value: '请参考正版'
					},{
						title: '宿舍楼',
						value: '8/7A/7B/12'
					},{
						title: '床位号',
						value: '5'
					},{
						title: '学生宿舍',
						value: '5-555'
					},{
						title: '原因',
						value: '请填写请假原因'
					},{
						title: '班长姓名',
						value: '张三'
					},{
						title: '年龄',
						value: '18'
					},{
						title: '学生手机',
						value: '150********'
					},{
						title: '家长手机',
						value: '150********'
					},{
						title: '外出地点',
						value: '旗岭'
					},{
						title: '班主任姓名',
						value: '李四'
					},{
						title: '班主任审核意见',
						value: '同意出去xxxx'
					},{
						title: '班主任审核时间',
						value: '格式：2021-01-01 12:30:15'
					},{
						title: '系主任姓名',
						value: '王五'
					},{
						title: '班主任审核时间',
						value: '格式：2021-01-01 12:30:15'
					},
					
				]
			}
		},
		methods: {
			preservation(){
				uni.setStorage({
				    key: 'leaveData',
				    data: 'hello',
				    success(res) {
				        console.log(res);
				    }
				});
			}
		}
	}
</script>

<style>
	.content {
		margin-bottom: 100rpx;
	}
	
	.content .item {
		display: flex;
		font-size: 26rpx;
		padding: 10rpx 0;
		border-bottom: 3rpx solid #dcdcdc;
	}
	
	.item .title {
		flex: 1;
		color: #27ae62;
		padding: 28rpx 0;
		text-align: right;
	}
	
	.item .value {
		flex: 2;
		color: #737373;
		padding: 28rpx 0 28rpx 20rpx;
	}
	
	.content button {
		color: #fff;
		background-color: #27AE62;
		margin-top: 80rpx;
	}
</style>
