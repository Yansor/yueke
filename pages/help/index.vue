<template>
	<view class="u-demo">
		<view class="u-demo-wrap" style="background-color: #ffffff;">
			<u-collapse v-if="key" :item-style="itemStyle" :body-style="bodyStyle" @change="change">
				<u-collapse-item :index="index" @change="itemChange" :title="item.head" v-for="(item, index) in itemList" :key="index" :class="u-border-bottom">
					<view class="item-wrap">
						<view class="title">如何登录学堂在线?</view>
						<view class="body">{{item.body}}</view>
						<u-line color="#D1D1D1" class="u-m-t-15 u-m-b-15"></u-line>
					</view>
					<view class="item-wrap">
						<view class="title">如何登录学堂在线?</view>
						<view class="body">{{item.body}}</view>
						<u-line color="#D1D1D1" class="u-m-t-15 u-m-b-15"></u-line>
					</view>
					<view class="item-wrap">
						<view class="title">如何登录学堂在线?</view>
						<view class="body">{{item.body}}</view>
						<u-line color="#D1D1D1" class="u-m-t-15 u-m-b-15"></u-line>
					</view>
					<view class="item-wrap">
						<view class="title">如何登录学堂在线?</view>
						<view class="body">{{item.body}}</view>
						<u-line color="#D1D1D1" class="u-m-t-15 u-m-b-15"></u-line>
					</view>
				</u-collapse-item>
			</u-collapse>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				itemList: [{
					head: "账号问题",
					body: "只要我们正确择取一个合适的参照物乃识的东西便会扑面而来：闪光的道德、妙异的智慧、优美的人情…… 赏识不是单向的施舍，是智慧与智慧的主动碰撞",
					show: false,
				}, {
					head: "认证问题",
					body: "学会欣赏，实际是一种积极生活的态度，是生活的调味品，会在欣赏中发现生活的美",
					show: false,
				}, {
					head: "课程问题",
					body: "但是据说雕刻大卫像所用的这块大理石，曾被多位雕刻家批评得一无是处，有些人认为这块大理石采凿得不好，有些人嫌它的纹路不够美，用它绝对雕不出好的艺术品，总之它被批评为一块不受人赏识的普通石头",
					show: false,
				}],
				hoverClass: 'hover2',
				itemStyle: {
					color: "red"
				},
				bodyStyle: {
					//height: '100rpx',
				},
				key: true
			}
		},
		onShow() {
			this.bodyStyle = {
				//overflow: 'hidden'
			}
		},
		methods: {
			itemChange(e) {
				console.log(e);
			},
		}
	}
</script>

<style lang="scss" scoped>
	.u-demo {
		padding: 20rpx;
	}
	
	.u-demo-wrap ::v-deep .u-collapse-item {
		border-bottom: 1rpx solid #F1F1F1;
		padding: 15rpx 0;
	}
	.u-demo-wrap ::v-deep .u-collapse-title {
		font-weight: bold;	
		font-size: 36rpx;
	}
	.u-demo-wrap ::v-deep .u-collapse-content {
		padding: 0 0 20rpx 0;
	}
	.u-demo-wrap .title {
		font-size: 32rpx;
		line-height: 60rpx;
		color: #333333;
	}
	
	.u-demo-wrap .title {
		line-height: 60rpx;
	}
	
</style>
