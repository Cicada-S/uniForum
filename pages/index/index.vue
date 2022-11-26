<template>
	<view id="index" class="container">
		<!-- 页面 header 相关部分 -->
		<view class="headerBox">
			<!-- 顶部广告位轮播图 -->
			<swiper class="swiper" :indicator-dots="false" :autoplay="true" :interval="3000" :duration="500">
				<swiper-item>
					<navigator url="http://baidu.com" open-type="navigate">
						<image class="bannerSwiperImg" src="@/static/images/index/swiper1.jpg" mode="aspectFill" />
					</navigator>
				</swiper-item>
				<swiper-item>
					<navigator url="http://baidu.com" open-type="navigate">
						<image class="bannerSwiperImg" src="@/static/images/index/swiper2.jpg" mode="aspectFill" />
					</navigator>
				</swiper-item>
				<swiper-item>
					<navigator url="http://baidu.com" open-type="navigate">
						<image class="bannerSwiperImg" src="@/static/images/index/swiper3.jpg" mode="aspectFill" />
					</navigator>
				</swiper-item>
			</swiper>
			<!-- 遮罩使用弧形框 -->
			<image class="crile" src="@/static/images/index/crile.png" mode="aspectFill" />
			<!-- 两个选项按钮 -->
			<view class="cardHeader">
				<view class="cardOne cardLeft">
					<image class="img" src="@/static/images/index/coffee.png" mode="widthFix">
					<view class="iright">
						<view class="title">精彩动态</view>
					</view>
				</view>
				<view class="cardOne cardRight">
					<image class="img" src="@/static/images/index/ran.png" mode="widthFix">
					<view class="iright">
						<view class="title">个人中心</view>
					</view>
				</view>
			</view>
			<!-- Tab 选项卡 -->
			<view class="tabsBox">
				<view class="oneNav navActived">推荐</view>
				<view class="oneNav">资讯</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	#sns {
		background-color: #F1F1F1;
	}

	// Header
	.headerBox {
		position: relative;
		left: 0;
		height: 500upx;
		background-color: #f1f1f1;
		z-index: 1;

		// 广告位轮播器相关样式
		.swiper {
			width: 750upx;
			height: 400upx;
			position: absolute;
			left: 0;
			top: 0;
			text-align: center;
			z-index: 1;

			.bannerSwiperImg {
				width: 750upx;
				height: 400upx;
				box-shadow: 0 0 2px 0 rgb(188, 188, 188);
			}
		}

		// 圆角遮挡
		.crile {
			width: 750upx;
			height: 50upx;
			position: absolute;
			left: 0;
			top: 355upx;
			z-index: 9;
		}

		// 新鲜事 活动墙 按钮样式
		.cardHeader {
			position: absolute;
			left: 0;
			top: 320upx;
			height: 160upx;
			z-index: 99;
			width: 710upx;
			margin-left: 20upx;
			display: flex;
			flex-direction: row;
			flex-wrap: wrap;
			justify-content: space-between;
			align-items: center;
			align-content: center;

			.cardOne {
				width: 328upx;
				height: 96upx;
				border-radius: 49upx;
				background-color: #FFFFFF;
				margin: 0 10upx;
				box-shadow: 0 0 2px 0 rgb(188, 188, 188);
				display: flex;
				flex-direction: row;
				flex-wrap: wrap;
				justify-content: flex-start;
				align-items: center;
				align-content: center;

				.img {
					width: 44upx;
					height: 44upx;
					margin-left: 50upx;
				}

				.iright {
					margin-left: 30upx;
					text-align: left;
					color: #888;

					.title {
						font-size: 30upx;
						color: #001432;
					}

					.iview {
						display: flex;
						flex-direction: row;
						flex-wrap: wrap;
						justify-content: space-between;
						align-items: center;
						align-content: center;
						font-size: 20upx;
						margin-top: -5upx;
					}
				}
			}
		}

		// 推荐、咨询 按钮样式
		.tabsBox {
			width: 750upx;
			position: absolute;
			z-index: 1;
			left: 0;
			top: 480upx;
			display: flex;
			flex-direction: row;
			justify-content: center;

			.oneNav {
				height: 80upx;
				width: 110upx;
				color: #9B9B9B;
				font-size: 36upx;
				text-align: center;
				font-weight: blod;

				&.navActived {
					color: #0050FF;
				}
			}
		}
	}

	// 
</style>
