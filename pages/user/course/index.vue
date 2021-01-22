<template>
	<view class="u-demo">
		<view class="u-demo-wrap">
			<view class="u-demo-head">
				<view>
					<view>9</view>
					<view>剩余课时</view>
				</view>
				<view>
					<block>
						<block>
							<block>9</block>
							<view>剩余课时</view>
						</block>
					</block>
					<block>
						<block>
							<block>9</block>
							<view>剩余课时</view>
						</block>
						
					</block>
				</view>
			
			</view>
			<view class="u-demo-area" >
				<u-tabs v-if="control" bg-color="#fafafa" :bold="bold" :active-color="activeColor" :list="list"
				@change="change" :current="current" :is-scroll="isScroll" :offset="offset"></u-tabs>
			</view>
			<view class="u-demo-contain">
				<view class="list-wrap" v-show="showContent">
					<u-cell-group>
						<u-cell-item :title-style="titleStyle" label="2021-01-01" title="老师周红" @click="openPage('/pages/user/course/index')">等待上课</u-cell-item>
						<u-cell-item :title-style="titleStyle" label="2021-01-01" title="老师周红">等待上课</u-cell-item>
						<u-cell-item :title-style="titleStyle" label="2021-01-01" title="老师周红">等待上课</u-cell-item>
						<u-cell-item :title-style="titleStyle" label="2021-01-01" title="老师周红">等待上课</u-cell-item>
						<u-cell-item :title-style="titleStyle" label="2021-01-01" title="老师周红">等待上课</u-cell-item>
						<u-cell-item :title-style="titleStyle" label="2021-01-01" title="老师周红" @click="openPage('/pages/user/edit')">等待上课</u-cell-item>
					</u-cell-group>
				</view>
				<view class="list-wrap" v-show="!showContent">
					<u-table align="center" :borderColor="borderColor">
						<u-tr class="u-tr">
							<u-td class="u-td">2020-01-01 08:08</u-td>
							<u-td class="u-td" width="20%">-12221133</u-td>
							<u-td class="u-td" width="40%">上课消耗</u-td>
						</u-tr>
						<u-tr class="u-tr">
							<u-td class="u-td">2020-01-01 08:08</u-td>
							<u-td class="u-td" width="20%">-12221133</u-td>
							<u-td class="u-td" width="40%">上课消耗</u-td>
						</u-tr>
						<u-tr class="u-tr">
							<u-td class="u-td">2020-01-01 08:08</u-td>
							<u-td class="u-td" width="20%">-12221133</u-td>
							<u-td class="u-td" width="40%">上课消耗</u-td>
						</u-tr>
					</u-table>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [],
				data: [{
					name: '约课记录',
					count: ''
				}, {
					name:  '消耗记录',
					count: ''
				}],
				current: 0,
				sectionCurrent: 0,
				isScroll: false, 
				tabCountIndex: 0,
				activeColor: "#000",
				bold: true,
				control: true,
				offset: [1, -1],
				
				showContent: true,
				titleStyle: {
					fontSize: "32rpx",
					color: "#000"
				},
				borderColor: '#e4e7ed',
			}
		},
		onLoad() {
			this.list = this.data;
		},
		methods: {
			change(index) {
				this.current = index;
				this.showContent = !this.showContent;
			},
		}
	}
</script>

<style lang="scss" scoped>
	.u-config-wrap {

	}
	.show {
		display: block;
		transition: .3s;
	}
	.hide {
		display: none;
		transition: .3s;
	}
	.u-demo-head {
		text-align: center;
	}
	.item {
		display: flex;
		padding: 20rpx;
	}
	image {
		width: 120rpx;
		flex: 0 0 120rpx;
		height: 120rpx;
		margin-right: 20rpx;
		border-radius: 12rpx;
	}
</style>
