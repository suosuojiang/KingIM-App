<template>
	<view>
		<com-cell :titles="titles"></com-cell>
		<com-cell :titles="titles"></com-cell>
		<com-cell :titles="titles"></com-cell>
	</view>
</template>

<script>
	import comCell from "@/components/com-Cell/com-Cell.vue";
	export default {
		data() {
			return {
				titles: 'suossuo'
			}
		},
		name:'chat',
		components: {
			comCell
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
