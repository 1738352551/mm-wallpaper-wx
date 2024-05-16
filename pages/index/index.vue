<template>
	<view class="homeLayout pageBG">
		<view class="banner">
			<swiper circular indicator-dots 
			indicator-color="rgba(255, 255, 255,.5)"
			indicator-active-color="#fff"
			duration="1000"
			autoplay>
				<swiper-item v-for="item in 3">
					<image src="../../common/images/banner1.jpg" mode="aspectFill" />
				</swiper-item>
			</swiper>
		</view>
		<man-notice />
		
		
		<view class="recommend-card">
			<man-common-title title="日常推荐">
				<template #custom>
					<view class="date">
						<uni-icons type="calendar" size="18"></uni-icons>
						<uni-dateformat :date="Date.now()" format="dd号"></uni-dateformat>
					</view>
				</template>
			</man-common-title>
			<view class="content">
				<scroll-view scroll-x>
					<view class="box" v-for="item in 8">
						<image src="../../common/images/preview_small.webp" mode="aspectFill"></image>
					</view>
				</scroll-view>
			</view>
		</view>
		
		
		<view class="special-topics">
			<man-common-title title="专题精选">
				<template #custom>
					<navigator class="more" url="">More+</navigator>
				</template>
			</man-common-title>
			
			<view class="content">
				<theme-item v-for="item in 8"></theme-item>
				<theme-item isMore></theme-item>
			</view>
		</view>
		
		
	</view>
</template>

<script setup>

</script>

<style scoped lang="scss">
.homeLayout {
	.banner {
		width: 750rpx;
		padding: 30rpx 0;
		swiper {
			width: 100%;
			height: 340rpx;
			&-item {
				height: 100%;
				width: 100%;
				padding: 0 30rpx;
				image {
					height: 100%;
					width: 100%;
					border-radius: 15rpx;
				}
			}
		}
	}
	
	.recommend-card {
		width: 730rpx;
		padding: 30rpx;
		scroll-view {
			white-space: nowrap;
			margin-top: 30rpx;
			.box {
				display: inline-block;
				width: 200rpx;
				height: 430rpx;
				margin-right: 15rpx;
				image {
					width: 100%;
					height: 100%;
					border-radius: 10rpx;
				}
			}
			.box:last-child {
				margin-right: 30rpx;
			}
		}
	}
	.special-topics {
		padding: 50rpx 30rpx;
		.content {
			margin-top: 30rpx;
			display: grid;
			grid-template-columns: repeat(3, 1fr);
			gap: 15rpx;
			
		}
	}

	.date {
		color: $brand-theme-color;
		:deep() {
			.uni-icons {
				color: $brand-theme-color !important;
			}
		}
	}
	.more {
		font-size: 24rpx;
		color: #888;
	}
	
}
</style>
