<template>
	<view class="themeItem">
		<navigator url="" class="box" v-if="!isMore">
			<image class="pic" src="../../common/images/classify1.jpg" mode="aspectFill"></image>
			<view class="mask">
				明星美女
			</view>
			<view class="tab">
				3天前更新
			</view>
		</navigator>
		
		<navigator url="" class="box more" v-else>
			<image class="pic" src="../../common/images/more.jpg" mode="aspectFill"></image>
			<view class="mask">
				<uni-icons type="more-filled" size="34" color="#fff"></uni-icons>
				<text>更多</text>
			</view>
		</navigator>
	</view>
</template>

<script setup>

defineProps({
	isMore: {
		type: Boolean,
		default: false
	}
})
</script>

<style lang="scss" scoped>
.themeItem {
	.box {
		height: 340rpx;
		border-radius: 10rpx;
		overflow: hidden;
		position: relative;
		.pic {
			width: 100%;
			height: 100%;
		}
		.mask {
			width: 100%;
			height: 70rpx;
			font-size: 30rpx;
			position: absolute;
			bottom: 0;
			left: 0;
			background: rgba(0,0,0,0.2);
			color: #fff;
			display: flex;
			align-items: center;
			justify-content: center;
			font-weight: bold;
			// 磨砂效果
			backdrop-filter: blur(20rpx);
		}
		
		.tab {
			position: absolute;
			left: 0;
			top: 0;
			background: rgba(250, 129, 90, 0.7);
			backdrop-filter: blur(20rpx);
			-webkit-backdrop-filter: blur(20rpx);
			color: #fff;
			font-size: 22rpx;
			padding: 6rpx 14rpx;
			border-radius: 0 0 20rpx 0;
		}
		
		&.more {
			.mask {
				width: 100%;
				height: 100%;
				flex-direction: column;
			}
			text {
				font-size: 28rpx;
			}
		}
	}
}
</style>