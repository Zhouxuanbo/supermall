<template>
  <div id="home">
    <NavBar class="home-nav"><div slot="middle">购物街</div></NavBar>
    <HomeSwiper :banner="banner"></HomeSwiper>
    <RecommandView :recommend="recommend"></RecommandView>
  </div>
</template>

<script>
import NavBar from "@/components/common/navbar/NavBar";
import HomeSwiper from "@/views/home/childComps/HomeSwiper";
import RecommandView from "@/views/home/childComps/RecommandView";
import {getHomeMultidata} from "@/network/home";

export default {
  name: "Home",
  components: {
    NavBar,
    HomeSwiper,
    RecommandView
  },
  data() {
    return {
      banner: [],
      recommend: []
    }
  },
  created() {
    getHomeMultidata().then(res => {
      this.banner = res.data.banner.list
      this.recommend = res.data.recommend.list
      console.log(this.recommend);
    })
  }
}
</script>

<style scoped>
  .home-nav {
    color: #f6f6f6;
    background-color: var(--color-tint);
  }
</style>
