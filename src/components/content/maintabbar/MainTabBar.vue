<template>
		<tab-bar>
			<tab-bar-item path="/home">
			<!-- html中要加别名需要添加~ -->
				<img src="~assets/img/tabbar/normal/home.svg" slot="item-icon" />
				<img src="~assets/img/tabbar/active/home.svg" slot="item-icon-active" />
				<div slot="item-text">首页</div>
			</tab-bar-item>
			<tab-bar-item path="/category">
				<img src="~assets/img/tabbar/normal/category.svg" slot="item-icon" />
				<img src="~assets/img/tabbar/active/category.svg" slot="item-icon-active" />
				<div slot="item-text">分类</div>
			</tab-bar-item>
			<tab-bar-item path="/cart">
				<img src="~assets/img/tabbar/normal/cart.svg" slot="item-icon" />
				<img src="~assets/img/tabbar/active/cart.svg" slot="item-icon-active" />
				<div slot="item-text">购物车</div>
			</tab-bar-item>
			<tab-bar-item path="/profile">
				<img src="~assets/img/tabbar/normal/profile.svg" slot="item-icon" />
				<img src="~assets/img/tabbar/active/profile.svg" slot="item-icon-active" />
				<div slot="item-text">我的</div>
			</tab-bar-item>
		</tab-bar>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from 'components/common/tabbar/TabBarItem'
export default {
	name: 'MainTabBar',
	data() {
		return {}
	},
	components: {
		TabBar,
		TabBarItem
	}
}
</script>

<style  scoped>
</style>