<template>
	<view class="my">
		<u-cell-group>
			<u-cell-item icon="account" title="个人信息" @click="$u.route({ url: '/pages/my/userInfo' })" />
			<u-cell-item icon="search" title="业绩查询" @click="$u.route({ url: '/pages/my/performanceQuery' })" />
			<u-cell-item icon="order" title="兑现记录" @click="$u.route({ url: '/pages/my/cashRecords' })" />
			<u-cell-item icon="list-dot" title="业绩排名" @click="$u.route({ url: '/pages/my/ranking' })" />
		</u-cell-group>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	}
};
</script>

<style lang="scss"></style>
