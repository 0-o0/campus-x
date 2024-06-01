<template>
	<view class="bgue">
		<view class="about tn-safe-area-inset-bottom">

			<view class="top-backgroup">
				<image src='https://f004.backblazeb2.com/file/ptsuki/dff.png' mode='widthFix' class='backgroud-image'></image>
			</view>

			<view class="about__wrap">
				<!-- 头像用户信息 -->
				<view
					class="user-info__container tn-flex tn-flex-direction-column tn-flex-col-center tn-flex-row-center">
					<view class="user-info__avatar tn-bg-grey--light tn-flex tn-flex-col-center tn-flex-row-center">
						<view class="tn-shadow-blur"
							style="background-image:url('https://f004.backblazeb2.com/file/ptsuki/avt.png');width: 180rpx;height: 180rpx;background-size: cover;">
						</view>
						<!-- <view class="tn-icon-logo-tuniao" style="font-size: 140rpx;color: #01BEFF;"></view> -->
					</view>
					<view class="user-info__nick-name">Hpi</view>
				</view>

				<!-- banner start-->
				<!-- <view class="tn-flex tn-flex-wrap tn-padding-xs" @click="navHpiVue3">
        <view class="" style="width: 100%;">
          <view class="image-piccapsule tn-shadow-blur" style="background-image:url('https://resource.tuniaokj.com/images/capsule-banner/banner-Vue3.png');">
             <view class="image-capsule">
             </view>
           </view>  
        </view>  
      </view> -->
				<!-- banner end-->

				<view class="tn-margin-left tn-margin-right">

					<!-- 方式20 start-->
					<view class="tn-flex">
						<view class="tn-flex-1 about-shadow tn-bg-white"
							style="margin: 50rpx 15rpx 0 0;padding: 30rpx 0;">
							<view class="tn-flex tn-flex-direction-column tn-flex-row-center tn-flex-col-center">
								<view
									class="icon20__item--icon tn-flex tn-flex-row-center tn-flex-col-center tn-shadow-blur tn-bg-orangered tn-color-white">
									<view class="tn-icon-computer-fill"></view>
								</view>
								<view class="tn-text-center" style="font-size: 30rpx;">
									<uni-link href="https://o-x.icu" class="tn-text-ellipsis" text="O_O" showUnderLine="false"
																	color=""></uni-link>
								</view>
							</view>
						</view>
						<view class="tn-flex-1 about-shadow tn-bg-white"
							style="margin: 50rpx 0 0 15rpx;padding: 30rpx 0;">
							<view class="tn-flex tn-flex-direction-column tn-flex-row-center tn-flex-col-center">
								<view
									class="icon20__item--icon tn-flex tn-flex-row-center tn-flex-col-center tn-shadow-blur tn-bg-purplered tn-color-white">
									<view class="tn-icon-moon-fill"></view>
								</view>
								<view class="tn-text-center" style="font-size: 30rpx;">
									<uni-link href="https://mp.weixin.qq.com/s/g_3rqqhy3W50AFlA5NaVAg" class="tn-text-ellipsis" text="Doki同学" showUnderLine="false"
																	color=""></uni-link>
								</view>
							</view>
						</view>
					</view>

					<!-- 数据信息 -->
					<!-- <view class="tn-info__container tn-flex tn-flex-wrap tn-flex-col-center tn-flex-row-between">
          <block v-for="(item, index) in tuniaoData" :key="index">
            <view class="tn-info__item tn-flex tn-flex-direction-row tn-flex-col-center tn-flex-row-between about-shadow">
              <view class="tn-info__item__left tn-flex tn-flex-direction-row tn-flex-col-center tn-flex-row-left">
                <view class="tn-info__item__left--icon tn-flex tn-flex-col-center tn-flex-row-center" :class="[`tn-bg-${item.color}--light tn-color-${item.color}`]">
                  <view :class="[`tn-icon-${item.icon}`]"></view>
                </view>
                <view class="tn-info__item__left__content">
                  <view class="tn-info__item__left__content--title">{{ item.title }}</view>
                  <view class="tn-info__item__left__content--data tn-padding-top-xs">{{ item.value }}</view>
                </view>
              </view>
              <view class="tn-info__item__right">
                <view class="tn-info__item__right--icon">
                  <view class="tn-icon-code"></view>
                </view>
              </view>
            </view>
          </block>
        </view> -->

					<!-- 更多信息-->
					<view class="about-shadow tn-margin-top-lg tn-padding-top-sm tn-padding-bottom-sm">
						<tn-list-cell :hover="true" :unlined="true" :radius="true" :fontSize="30" @click="copyxjust">
							<view class="tn-flex tn-flex-col-center">
								<view
									class="icon1__item--icon tn-flex tn-flex-row-center tn-flex-col-center tn-cool-bg-color-1 tn-color-white">
									<view class="tn-icon-fire-fill"></view>
								</view>
								<view class="tn-margin-left-sm tn-flex-1">学校官网</view>
								<view class="tn-margin-left-sm tn-color-blue tn-icon-copy-fill"></view>
							</view>
						</tn-list-cell>
						<tn-list-cell :hover="true" :unlined="true" :radius="true" :fontSize="30" @click="copyblog">
							<view class="tn-flex tn-flex-col-center">
								<view
									class="icon1__item--icon tn-flex tn-flex-row-center tn-flex-col-center tn-cool-bg-color-3 tn-color-white">
									<view class="tn-icon-star-fill"></view>
								</view>
								<view class="tn-margin-left-sm tn-flex-1">学校微博</view>
								<view class="tn-margin-left-sm tn-color-blue tn-icon-copy-fill"></view>
							</view>
						</tn-list-cell>
						<tn-list-cell :hover="true" :unlined="true" :radius="true" :fontSize="30">
							<view class="tn-flex tn-flex-col-center">
								<view
									class="icon1__item--icon tn-flex tn-flex-row-center tn-flex-col-center tn-cool-bg-color-6 tn-color-white">
									<view class="tn-icon-safe-fill"></view>
								</view>
								<uni-link href="https://blog.o-x.icu" class="tn-margin-left-sm tn-flex-1" text="个人博客"
									showUnderLine="false" color=""></uni-link>
								<view class="tn-margin-left-sm tn-color-red tn-icon-send-fill"></view>
							</view>
						</tn-list-cell>
						<tn-list-cell :hover="true" :unlined="true" :radius="true" :fontSize="30">
							<view class="tn-flex tn-flex-col-center">
								<view
									class="icon1__item--icon tn-flex tn-flex-row-center tn-flex-col-center tn-cool-bg-color-2 tn-color-white">
									<view class="tn-icon-set-fill"></view>
								</view>
								<view class="tn-margin-left-sm tn-flex-1">基于Tunaio UI 开发</view>
								<view class="tn-margin-left-sm tn-color-gray">版本号1.0</view>
							</view>
						</tn-list-cell>
					</view>
					<!-- 更多信息-->
					<view
						class="about-shadow tn-margin-top-lg tn-margin-bottom-lg tn-padding-top-sm tn-padding-bottom-sm">
						<tn-list-cell :hover="true" :unlined="true" :radius="true" :fontSize="30">
							<button class="tn-flex tn-flex-col-center tn-button--clear-style" open-type="contact">
								<view
									class="icon1__item--icon tn-flex tn-flex-row-center tn-flex-col-center tn-cool-bg-color-9 tn-color-white">
									<view class="tn-icon-wechat-fill"></view>
								</view>
								<view class="tn-margin-left-sm">交流群</view>
							</button>
						</tn-list-cell>
						<tn-list-cell :hover="true" :unlined="false" :radius="true" :fontSize="30">
							<view class="tn-flex tn-flex-col-center tn-button--clear-style" open-type="feedback">
								<view
									class="icon1__item--icon tn-flex tn-flex-row-center tn-flex-col-center tn-cool-bg-color-13 tn-color-white">
									<view class="tn-icon-comment-fill"></view>
								</view>
								<uni-link href="http://wpa.qq.com/msgrd?v=3&uin=1341361765&site=qq&menu=yes"
									class="tn-margin-left-sm" text="问题反馈" showUnderLine="false" color=""></uni-link>
							</view>
						</tn-list-cell>
					</view>
				</view>
			</view>


			<view class="tn-padding-bottom-xs"></view>

		</view>
	</view>
</template>

<script>
	export default {
		name: 'Hpi',
		data() {
			return {
				hpiData: [{
						title: 'View',
						icon: 'eye',
						color: 'indigo',
						value: '1.22 W'
					},
					{
						title: 'Star',
						icon: 'star',
						color: 'orange',
						value: '406'
					},
					{
						title: 'Fork',
						icon: 'fork',
						color: 'purplered',
						value: '129'
					},
					{
						title: 'Version',
						icon: 'trusty',
						color: 'green',
						value: '1.2.0'
					}
				],
			}
		},
		methods: {


			// xue
			copyDCloud() {
				uni.setClipboardData({
					data: "https://xjust.edu.cn",
				})
			},

			// wei
			copyblog() {
				uni.setClipboardData({
					data: "https://www.weibo.com/u/6068076929",
				})
			},

		}
	}
</script>

<style lang="scss" scoped>
	.bgue {
		position: relative;
		z-index: 1;
		margin: 0rpx 0rpx;
		margin-top: -100;
	}

	/* 顶部背景图 start */
	.top-backgroup {
		height: 450rpx;
		z-index: -1;

		.backgroud-image {
			width: 100%;
			height: 967rpx;
			// z-index: -1;
		}
	}

	/* 顶部背景图 end */

	/* 页面 start*/
	.about-shadow {
		border-radius: 15rpx;
		box-shadow: 0rpx 0rpx 50rpx 0rpx rgba(0, 0, 0, 0.07);
	}

	.about {

		&__wrap {
			position: relative;
			z-index: 1;
			margin: 20rpx 0rpx;
			margin-top: -180rpx;
		}
	}

	/* 页面 end*/

	/* 用户信息 start */
	.user-info {
		&__container {}

		&__avatar {
			width: 180rpx;
			height: 180rpx;
			border: 8rpx solid rgba(255, 255, 255, 0.05);
			border-radius: 50%;
			overflow: hidden;
			box-shadow: 0rpx 0rpx 80rpx 0rpx rgba(0, 0, 0, 0.15);
		}

		&__nick-name {
			margin-top: 26rpx;
			font-size: 42rpx;
			font-weight: 600;
			text-align: center;
		}
	}

	/* 用户信息 end */

	/* 信息展示 start */
	.tn-info {

		&__container {
			margin-top: 0rpx;
		}

		&__item {
			width: 48%;
			margin: 15rpx 0rpx;
			padding: 28rpx;
			border-radius: 15rpx;


			position: relative;
			z-index: 1;

			&::after {
				content: " ";
				position: absolute;
				z-index: -1;
				width: 100%;
				height: 100%;
				left: 0;
				bottom: 0;
				border-radius: inherit;
				opacity: 1;
				transform: scale(1, 1);
				background-size: 100% 100%;
				background-image: url(https://resource.tuniaokj.com/images/cool_bg_image/6.png);
			}

			&__left {

				&--icon {
					width: 80rpx;
					height: 80rpx;
					border-radius: 50%;
					font-size: 40rpx;
					margin-right: 20rpx;
					position: relative;
					z-index: 1;

					&::after {
						content: " ";
						position: absolute;
						z-index: -1;
						width: 100%;
						height: 100%;
						left: 0;
						bottom: 0;
						border-radius: inherit;
						opacity: 1;
						transform: scale(1, 1);
						background-size: 100% 100%;
						background-image: url(https://resource.tuniaokj.com/images/cool_bg_image/icon_bg5.png);
					}
				}

				&__content {
					font-size: 30rpx;

					&--data {
						margin-top: 5rpx;
						font-weight: bold;
					}
				}
			}

			&__right {
				&--icon {
					font-size: 60rpx;
					opacity: 0.15;
				}
			}
		}
	}

	/* 信息展示 end */

	/* 图标容器5 start */
	.icon5 {
		&__item {
			// width: 30%;
			background-color: #FFFFFF;
			border-radius: 10rpx;
			padding: 0rpx;
			margin: 0rpx;
			transform: scale(1);
			transition: transform 0.3s linear;
			transform-origin: center center;

			&--icon {
				width: 100rpx;
				height: 100rpx;
				border-radius: 50%;
				margin-bottom: 18rpx;
				position: relative;
				z-index: 1;
			}
		}
	}

	.icon20 {
		&__item {
			width: 30%;
			background-color: #FFFFFF;
			border-radius: 10rpx;
			padding: 30rpx;
			margin: 20rpx 10rpx;
			transform: scale(1);
			transition: transform 0.3s linear;
			transform-origin: center center;

			&--icon {
				width: 100rpx;
				height: 100rpx;
				font-size: 60rpx;
				border-radius: 50%;
				margin-bottom: 18rpx;
				position: relative;
				z-index: 1;

				&::after {
					content: " ";
					position: absolute;
					z-index: -1;
					width: 100%;
					height: 100%;
					left: 0;
					bottom: 0;
					border-radius: inherit;
					opacity: 1;
					transform: scale(1, 1);
					background-size: 100% 100%;
					background-image: url(https://resource.tuniaokj.com/images/cool_bg_image/icon_bg.png);
				}
			}
		}
	}

	/* 图标容器1 start */
	.icon1 {
		&__item {
			// width: 30%;
			background-color: #FFFFFF;
			border-radius: 10rpx;
			padding: 30rpx;
			margin: 20rpx 10rpx;
			transform: scale(1);
			transition: transform 0.3s linear;
			transform-origin: center center;

			&--icon {
				width: 40rpx;
				height: 40rpx;
				font-size: 28rpx;
				border-radius: 50%;
				position: relative;
				z-index: 1;

				&::after {
					content: " ";
					position: absolute;
					z-index: -1;
					width: 100%;
					height: 100%;
					left: 0;
					bottom: 0;
					border-radius: inherit;
					opacity: 1;
					transform: scale(1, 1);
					background-size: 100% 100%;
					background-image: url(https://resource.tuniaokj.com/images/cool_bg_image/icon_bg.png);
				}
			}
		}
	}

	/* 图标容器1 end */

	/* 胶囊banner*/
	.image-capsule {
		padding: 100rpx 0rpx;
		font-size: 40rpx;
		font-weight: 300;
		position: relative;
	}

	.image-piccapsule {
		background-size: cover;
		background-repeat: no-repeat;
		// background-attachment:fixed;
		background-position: top;
		border-radius: 20rpx 20rpx 0 0;
	}
</style>