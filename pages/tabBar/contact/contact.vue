<template>
	<view>
		<com-cell mode="friend"></com-cell>
		<com-cell mode="friend"></com-cell>
		<com-cell mode="friend"></com-cell>
		<com-cell mode="friend"></com-cell>
		<view class="type">星标朋友</view>
		<com-cell mode="friend"></com-cell>
		<view class="type">A</view>
		<com-cell mode="friend"></com-cell>
		<view class="type">B</view>
		<com-cell mode="friend"></com-cell>
		<view class="end">{{nums}}位联系人</view>
		<contact-alphabet></contact-alphabet>
	</view>
</template>

<script>
	import comCell from "@/components/com-Cell/com-Cell.vue";
	import contactAlphabet from "@/components/contact-Alphabet/contact-Alphabet.vue";
	export default {
		data() {
			return {
				nums: 400
			}
		},
		components: {
			comCell,
			contactAlphabet
		},
		methods: {
			
		}
	}
</script>

<style scoped lang="scss">
	.type{
		width: 100%;
		height: 50rpx;
		line-height: 50rpx;
		font-size: 16rpx;
		color: #808080;
		background: #f1f1f1;
		padding: 0 30rpx;
	}
	.end{
		color: #808080;
		height: 100rpx;
		line-height: 100rpx;
		font-size: 32rpx;
		text-align: center;
	}
</style>
