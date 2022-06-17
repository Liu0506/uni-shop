<template>
	<view>
		<!--  #ifdef  APP-PLUS -->
		<view class="status-bar"></view>
		<!--  #endif -->
		<uni-nav-bar :fixed="true" left-icon="search">
			<view class="hd-nav-center"><text>快乐商城</text></view>
			<template v-slot:right>
				<view>
					<uni-icons type="chatbubble" size="20"></uni-icons>
					<view class="hd-nav-right">99+</view>
				</view>
			</template>
		</uni-nav-bar>
	</view>
</template>

<script>
	export default {
		name: "homeNav"
	}
</script>

<style scoped lang="scss">
	/*  #ifdef  APP-PLUS || H5  */
	.status-bar {
		height: var(--status-bar-height);
		width: 100%;
	}

	/*  #endif  */

	.hd-nav-center {
		display: flex;
		width: 100%;
		justify-content: center;
		align-items: center;
		font-size: 16px;
		font-weight: bold;
	}

	.hd-nav-right {
		position: absolute;
		right: 0;
		top: 0;
		width: 26px;
		height: 26px;
		border-radius: 50%;
		background-color: orangered;
		text-align: center;
		line-height: 26px;
		color: #fff;
		font-size: 12px;
		transform: scale(.6, .6);
	}
</style>
