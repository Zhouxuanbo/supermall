<template>
  <TabBar>
    <TabBarItem path="/home" activeColor="#3f7ee6">
      <img slot="item png" src="@/assets/img/tabbar/home.png" alt="">
      <img slot="item-png-active" src="@/assets/img/tabbar/home-active.png" alt="">
      <div slot="item text">首页</div>
    </TabBarItem>
    <TabBarItem path="/category" activeColor="purple">
      <img slot="item png" src="@/assets/img/tabbar/category.png" alt="">
      <img slot="item-png-active" src="@/assets/img/tabbar/category-active.png" alt="">
      <div slot="item text">分类</div>
    </TabBarItem>
    <TabBarItem path="/cart" activeColor="#dede22">
      <img slot="item png" src="@/assets/img/tabbar/shopcart.png" alt="">
      <img slot="item-png-active" src="@/assets/img/tabbar/shopcart-active.png" alt="">
      <div slot="item text">购物车</div>
    </TabBarItem>
    <TabBarItem path="/profile" activeColor="#33e0e0">
      <img slot="item png" src="@/assets/img/tabbar/profile.png" alt="">
      <img slot="item-png-active" src="@/assets/img/tabbar/profile-active.png" alt="">
      <div slot="item text">我的</div>
    </TabBarItem>
  </TabBar>
</template>

<script>
import TabBar from "@/components/common/tabbar/TabBar";
import TabBarItem from "@/components/common/tabbar/TabBarItem";
export default {
  name: "MainTabBar",
  components: {
    TabBarItem,
    TabBar
  }
}
</script>

<style scoped>

</style>
