<template>
	<ul class="list">
		<li class="list__item">A</li>
		<li class="list__item">B</li>
		<li class="list__item">C</li>
		<li class="list__item">D</li>
	</ul>
</template>

<script>
	export default {
		name: 'contactAlphabet',
		props: {
			hasDots: {
				type: Boolean,
				default: true
			},
			titles: {
				type: String,
				default: ''
			}
		},
		data() {
			return {
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
	.list{
		display: flex;
		flex-direction: column;
		justify-content: center;
		position: absolute;
		top: 0;
		right: 0;
		bottom: 0;
		width: 30rpx;
		list-style: none;
		font-size: 28rpx;
		// background: pink;
		text-align: center;
		
		&__item{
			color: rgb(0, 203, 143);
		}
	}
</style>