<template>
	<view class="container">
		<image src="https://t.alcy.cc/moez" mode="aspectFill" @click="openUrl('**jwmobile/index')"
			style="width: 100%; height: 100%; object-fit: cover;"></image>
		<web-view v-if="webViewUrl" :src="webViewUrl" :style="{ height: webviewHeight + 'px'}"></web-view>
		<!-- <view @click="close" class="close">X</view> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				webviewHeight: 0,
				webViewUrl: ''
			}
		},
		mounted() {
			uni.getSystemInfo({
				success: (sysinfo) => {
					this.webviewHeight = sysinfo.windowHeight - 52; //
				}
			});
		},
		methods: {
			openUrl(url) {
				this.webViewUrl = url;
			},
			close() {
				// 返回上一层界面
				uni.navigateBack({
					delta: 0
				});
			}
		}
	};
</script>

<style scoped>
	.container {
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
	}

	.web-content {
		width: 100%;
		position: absolute;
		top: 0;
		bottom: 52px;
	}

	.close {
		position: absolute;
		top: 0;
		left: 0;
		z-index: 9999;
		display: flex;
		align-items: center;
		justify-content: center;
		width: 30px;
		height: 30px;
		line-height: 30px;
		text-align: center;
		color: #cdcdcd;
		border: 2px solid ;
		border-radius: 50%;
		margin: 7px;
		cursor: pointer;
		font-family: Arial, sans-serif;
		font-weight: bold;
		font-size: 30px;
		text-transform: uppercase;
		background: linear-gradient(45deg, #007AFF, #884EA0);
		box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
		transition: all 0.3s ease;
	}



	.close:hover {
		transform: scale(1.05);
		box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
	}

	.close:active {
		transform: scale(0.95);
	}
</style>