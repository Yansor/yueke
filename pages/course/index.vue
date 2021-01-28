<template>
	<view class="u-demo">
		<view class="u-demo-wrap">
			<view class="u-demo-area">
				<u-cell-group>
					<u-cell-item :border-bottom="false" :border-top="false" center :is-link="true" :label="label" value="点击选择" :value-style="valueStyle" index="index" @click="click" :hover-class="hoverClass"
					 :arrow="arrow" :title="title" :title-style="titleStyle">
					</u-cell-item>
					<u-gap :height="gapHeight" :bg-color="bgColor"></u-gap>
					<u-cell-item :border-bottom="false" :border-top="false" center :is-link="true" :label="label" value="点击选择" :value-style="valueStyle" index="index" @click="click" :hover-class="hoverClass"
					 :arrow="arrow" :title="title" :title-style="titleStyle">
					</u-cell-item>
					<u-gap :height="gapHeight" :bg-color="bgColor"></u-gap>
					<u-cell-item :border-bottom="false" :border-top="false" center :is-link="true" :label="label" value="点击选择" :value-style="valueStyle" index="index" @click="click" :hover-class="hoverClass"
					 :arrow="arrow" :title="title"  :title-style="titleStyle">
					</u-cell-item>
					<u-gap :height="gapHeight" :bg-color="bgColor"></u-gap>
					<u-cell-item :border-bottom="false" :border-top="false" center :is-link="true" :label="label" value="点击选择" :value-style="valueStyle" index="index" @click="click" :hover-class="hoverClass"
					 :arrow="arrow" :title="title"  :title-style="titleStyle">
					</u-cell-item>
					<u-gap :height="gapHeight" :bg-color="bgColor"></u-gap>
					<u-cell-item :border-bottom="false" :border-top="false" center :is-link="true" :label="label" value="点击选择" :value-style="valueStyle" index="index" @click="click" :hover-class="hoverClass"
					 :arrow="arrow" :title="title"  :title-style="titleStyle">
					</u-cell-item>
				</u-cell-group>
			</view>
		</view>
		<view class="bottom">
			<u-button :custom-style="cancelStyle" :hair-line="hairLine" :shape="shape">取消</u-button>
			<u-button :custom-style="nextStyle" :hair-line="hairLine" :shape="shape">下一步</u-button>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				icon: '',
				arrow: false,
				label: '岂曰无衣，与子同裳',
				title: '青山一道同云雨',
				rightSlot: "switch",
				checked: false,
				bgColor: "#f7f7f7",
				gapHeight: 40,
				valueStyle: {},
				titleStyle: {
					color: "#000"
				},
				shape: "circle",
				hairLine: false,
				cancelStyle: {
					width: "180rpx",
					color: "#9f9f9f"
				},
				nextStyle: {
					width: "480rpx",
					backgroundColor: "#fae800",
					color: "#000",
					borer: "none"
				}
			}
		},
		computed: {
			hoverClass() {
				// 如果右侧是switch步进器组件的话，去掉cell的点击反馈，因为这个时候点击的反馈应该在switch上
				return this.rightSlot == 'switch' ? 'none' : 'u-cell-hover';
			}
		},
		methods: {
			iconChange(index) {
				this.icon = index == 0 ? 'setting' : 'file-text'
			},
			titleChange(index) {
				this.title = index == 0 ? '青山一道同云雨' : '明月何曾是两乡'
			},
			rightSlotChange(index) {
				this.rightSlot = index == 0 ? 'text' : index == 1 ? 'switch' : 'badge'
				if (index == 0) this.arrow = true;
				else this.arrow = false;
			},
			click(index) {
				// console.log(index);
			}
		}
	};
</script>

<style lang="scss" scoped>
	.u-demo {
	    padding: 25px 20px;
	}
	page {
		background-color: #f7f7f7;
	}
	.gab {
		background-color: rgb(245, 245, 245);
		height: 20rpx;
	}

	.wrap {
		height: 100vh;
		background-color: rgb(241, 241, 241);
	}

	.box {
		padding: 30rpx 00rpx;
		font-size: 28rpx;
		color: $u-type-info;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
	.bottom {
		background-color: #ffffff;
		align-items: center;
		position: relative;
		position: fixed;
		bottom: 0;
		left: 0;
		width: 100%;
		z-index: 998;
		display: flex;
		height: 160rpx;
	}
</style>