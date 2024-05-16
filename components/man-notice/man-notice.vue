<template>
	<view class="notice">
		<view class="left">
			<uni-icons type="sound-filled" size="20"></uni-icons>
			<text class="text">公告</text>
		</view>
		<view class="center">
			<swiper circular vertical autoplay
				duration="300" interval="1000"
			>
				<swiper-item>测试公告测试公告测试公告测试公告测试公告测试公告测试公告测试公告</swiper-item>
				<swiper-item>测试公告</swiper-item>
				<swiper-item>测试公告</swiper-item>
			</swiper>
		</view>
		<view class="right">
			<uni-icons type="forward" size="20"></uni-icons>
		</view>
	</view>
</template>

<script setup>

</script>

<style lang="scss" scoped>
	.notice {
		width: 690rpx;
		height: 80rpx;
		background-color: #f9f9f9;
		margin: 0 auto;
		display: flex;
		line-height: 80rpx;
		border-radius: 80rpx;
		.left {
			width: 140rpx;
			display: flex;
			justify-content: center;
			align-items: center;
			:deep() {
				.uni-icons {
					color: $brand-theme-color !important;
				}
			}
			.text {
				font-size: 28rpx;
				color: $brand-theme-color;
				font-weight: 600;
			}
		}
		
		.center {
			flex: 1;
			color: $text-font-color-2;
			swiper {
				height: 100%;
				&-item {
					font-size: 24rpx;
					overflow: hidden;
					text-wrap: nowrap;
					text-overflow: ellipsis;
				}
			}
		}
		
		.right {
			width: 70rpx;
			display: flex;
			justify-content: center;
			align-items: center;
		}
	}
</style>