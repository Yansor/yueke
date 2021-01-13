<template>
	<view class="yueke-index">
		<view class="yueke-swiper-area">
			<u-toast ref="uToast"></u-toast>
			<u-swiper @change="change" :height="250" :list="list" :title="title" :effect3d="effect3d" 
			:indicator-pos="indicatorPos" :mode="mode" :interval="3000" @click="click"></u-swiper>
		</view>
		<view class="yueke-star-student">
			<view class="item-wrap">
				<block class="item">
					<video class="item-video" id="myVideo" src="https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20200317.mp4"
					                    @error="videoErrorCallback" :danmu-list="danmuList" enable-danmu danmu-btn controls></video>
				</block>
				<block class="item">
					<video class="item-video" id="myVideo" src="https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20200317.mp4"
					                    @error="videoErrorCallback" :danmu-list="danmuList" enable-danmu danmu-btn controls></video>
				</block>
				<block class="item">
					<video class="item-video" id="myVideo" src="https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20200317.mp4"
					                    @error="videoErrorCallback" :danmu-list="danmuList" enable-danmu danmu-btn controls></video>
				</block>
				<block class="item">
					<video class="item-video" id="myVideo" src="https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20200317.mp4"
					                    @error="videoErrorCallback" :danmu-list="danmuList" enable-danmu danmu-btn controls></video>
				</block>
			</view>
			
		</view>
		
		
		
		
	</view>
</template>
	

<script>
	export default {
		data() {
			return {
				list: [{
						image: 'https://cdn.uviewui.com/uview/swiper/1.jpg',
						title: '昨夜星辰昨夜风，画楼西畔桂堂东'
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/2.jpg',
						title: '身无彩凤双飞翼，心有灵犀一点通'
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/3.jpg',
						title: '谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳'
					}
				],
				title: false,
				mode: 'round',
				indicatorPos: 'bottomCenter',
				effect3d: false,
				
			}
		},
		methods: {
			titleChange(index) {
				this.title = index == 0 ? true : false;
			},
			modeChange(index) {
				this.mode = index == 0 ? 'round' : index == 1 ? 'rect' : index == 2 ? 'number' : 'none';
			},
			indicatorPosChange(index) {
				this.indicatorPos = index == 0 ? 'topLeft' : index == 1 ? 'topRight' : index == 2 ? 'bottomLeft' : index == 3 ? 'bottomCenter'  : 'bottomRight';
			},
			effect3dChange(index) {
				this.effect3d = index == 0 ? true : false;
			},
			click(index) {
				this.$refs.uToast.show({
					title: `点击了第${index + 1}张图片`,
					type: 'success'
				})
			},
			change(index) {
				// console.log(index);
			}
		}
	}
</script>

<style lang="scss" scoped>
	.yueke-star-student {
		margin-top: 30rpx;
		overflow-x: scroll;
	}
	.item-wrap {
		width: 1400rpx;
	}
	.item {
		margin: 30rpx 0;
	}
	.item-video {
		margin-right: 30rpx;
		width: 300rpx;
		height: 200rpx;
		border-radius: 20rpx;;
	}
</style>

