<template>
	<view class="cell-container">
		<view class="cell" v-if="mode === 'chat'">
			<view class="cell__pic">
				<image class="cell__pic__img" :src="iconImg" mode="aspectFill"></image>
				<view class="cell__pic__dot" v-show="hasDots"></view>
			</view>
			<view class="cell__content">
				<view class="cell__content__title com-one-line">{{titles}}</view>
				<view class="cell__content__desc com-one-line">我最爱的小仙女呀呀呀我最爱的小仙女呀呀呀我最爱的小仙女呀呀呀我最爱的小仙女呀呀呀dsjfklsdjffdsfjlk</view>
				<view class="cell__content__time">11:40</view>
			</view>
		</view>
		<view class="cell" v-if="mode === 'friend'">
			<view class="cell__pic">
				<image class="cell__pic__img" :src="iconImg" mode="aspectFill"></image>
				<!-- <view class="cell__pic__dot" v-show="hasDots"></view> -->
			</view>
			<view class="cell__content">
				<view class="cell__content__title com-one-line">亲爱的梭梭酱</view>
				<!-- <view class="cell__content__desc com-one-line">我最爱的小仙女呀呀呀我最爱的小仙女呀呀呀我最爱的小仙女呀呀呀我最爱的小仙女呀呀呀dsjfklsdjffdsfjlk</view> -->
				<!-- <view class="cell__content__time">11:40</view> -->
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: 'comCell',
		props: {
			hasDots: {
				type: Boolean,
				default: true
			},
			mode: {
				type: String,
				default: 'chat'
			},
			iconImg: {
				type: String,
				default: '/static/logo.png'
			},
			titles: {
				type: String,
				default: ''
			}
		},
		data() {
			return {
				width: `display: inline-block;width: ${String(this.text).length * 15 + 25}rpx`
			};
		},
		methods: {
			onClick() {
				this.$emit('click');
			}
		}
	};
</script>

<style scoped lang="scss">
	.cell-container{
		.cell{
			width: 750rpx;
			box-sizing: border-box;
			padding: 0 25rpx;
			// margin-bottom: 30rpx;
			height: 140rpx;
			display: flex;
			align-items: center;
			
			&__pic{
				width: 100rpx;
				height: 100rpx;
				border-radius: 10px;
				margin-right: 20rpx;
				position: relative;
				
				&__img{
					width: 100rpx;
					height: 100rpx;
				}
				
				&__dot{
					width: 20rpx;
					height: 20rpx;
					background: red;
					border-radius: 10rpx;
					position: absolute;
					top: -10rpx;
					right: -10rpx;
				}
			}
			
			&__content{
				position: relative;
				width: 580rpx;
				height: 140rpx;
				border-bottom: 1rpx solid #f7f7f7;
				box-sizing: border-box;
				display: flex;
				flex-direction: column;
				justify-content: center;
				// padding-top: 6rpx;
				
				&__title{
					width: 460rpx;
					height: 50rpx;
					font-size: 32rpx;
				}
				
				&__desc{
					width: 560rpx;
					height: 40rpx;
					font-size: 28rpx;
					color: #999999;
				}
				
				&__time{
					position: absolute;
					right: 10rpx;
					top: 20rpx;
					font-size: 24rpx;
					color:#C0C0C0;
				}
			}
		}
	}
</style>