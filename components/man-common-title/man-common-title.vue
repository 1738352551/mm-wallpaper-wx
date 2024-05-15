<template>
	<view class="commonTitle">
		<view class="title">
			{{title}}
		</view>
		<view class="right">
			<slot name="custom"/>
		</view>
	</view>
</template>

<script setup>
import {defineProps} from 'vue';
defineProps({
	title: {
		type: String,
		required: true,
	},
})
</script>

<style lang="scss" scoped>
.commonTitle {
	display: flex;
	justify-content: space-between;
	align-items: center;
	// padding: 0 30rpx;
	.title {
		font-size: 40rpx;
	}
}
</style>