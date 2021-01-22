<template>
	<view>
		<view class="u-flex user-box u-p-l-30 u-p-r-20 u-p-b-30" @click="openPage('/pages/user/edit')">
			<view class="u-m-r-10">
				<u-avatar :src="pic" size="140"></u-avatar>
			</view>
			<view class="u-flex-1">
				<view class="u-font-18 u-p-b-20">周红</view>
				<view class="u-font-14 u-tips-color">UID:2347623</view>
			</view>
			<view class="u-m-l-10 u-p-10">
				<u-icon name="arrow-right" color="#969799" size="28"></u-icon>
			</view>
		</view>
		
		<view class="u-m-t-20">
			<u-cell-group>
				<u-cell-item icon="rmb-circle" title="我的约课"  @click="openPage('/pages/user/course/index')"></u-cell-item>
				<u-cell-item icon="star" title="课时记录" @click="openPage('/pages/user/edit')">345345</u-cell-item>
				<u-cell-item icon="photo" title="我的订单" @click="openPage('/pages/detail')"></u-cell-item>
				<u-cell-item icon="coupon" title="常见问题" @click="openPage('/pages/help/index')"></u-cell-item>
				<u-cell-item icon="heart" title="如何上课" @click="openPage('/pages/detail')"></u-cell-item>
				<u-cell-item icon="setting" title="关于我们" @click="openPage('/pages/detail')"></u-cell-item>
			</u-cell-group>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				pic:'https://uviewui.com/common/logo.png',
				show:true
			}
		},
		onLoad() {
			
		},
		methods: {
			openPage(path) {
				this.$u.route({
					url: path
				});
			}
		}
	}
</script>

<style lang="scss" scoped>


.camera{
	width: 54px;
	height: 44px;
	
	&:active{
		background-color: #ededed;
	}
}
.user-box{
	background-color: #fff;
}
</style>
