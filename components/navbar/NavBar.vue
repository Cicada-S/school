<template>
  <view class="nav-bar">
    <view class="left"><slot name="left"></slot></view>
    <view class="center"><slot name="center"></slot></view>
    <view class="right"><slot name="right"></slot></view>
  </view>
</template>

<script>
  export default {
    data() {
		return {
			
		}
	}
	methods: {
		
	}
  }
</script>

<style>
  .nav-bar {
    display: flex;
	padding: 40rpx;
    height: 88rpx;
    line-height: 88rpx;
    text-align: center;
  }

  .left, .right {
    width: 120rpx;
  }

  .center {
    flex: 1;
  }
</style>
