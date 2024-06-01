<template>
  <view class="webview-container">
    <!-- web-view 组件，直接设置为指定的URL -->
    <web-view ref="webview" :style="{ height: webviewHeight + 'px' }" src="**jwmobile/index"></web-view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      webviewHeight: 0 // 初始化web-view的高度为0
    };
  },
  mounted() {
    // 获取系统信息
    uni.getSystemInfo({
      success: (sysinfo) => {
        // 计算web-view的高度，减去底部导航栏的高度
        this.webviewHeight = sysinfo.windowHeight - 0; // 假设底部导航栏高度为50px
      }
    });
  }
};
</script>

<style scoped>
.webview-container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.web-content {
  width: 100%; /* 宽度占满容器 */
  position: absolute; /* 使用绝对定位 */
  top: 0;
  bottom: 0px; /* 保留底部导航栏的空间 */
}
</style>
